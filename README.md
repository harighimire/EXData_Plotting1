> setwd("C:/Users/ASUS/Desktop/R software/exdata_data_household_power_consumption")
> data_power <- read.csv("household_power_consumption.txt", header=TRUE, sep=';',nrows=2075259, na.strings="?", 
+                        check.names=F, stringsAsFactors=FALSE, comment.char="", quote='\"')
> 
> data_power$Date <- as.Date(data_power$Date, format="%d/%m/%Y")
> data <- subset(data_power, Date >= "2007-02-01" & Date <= "2007-02-02")
> View(data)
> datetime <- paste(as.Date(data$Date), data$Time)
> data$Datetime <- as.POSIXct(datetime)
> hist(data$Global_active_power, main="Global Active Power", 
+      xlab="Global Active Power (kilowatts)", ylab="Frequency", col="Red")
> plot(data$Global_active_power~data$Datetime, type="l", ylab="Global Active Power (kilowatts)", xlab="")
> with(data, {
+     plot(Sub_metering_1~Datetime, type="l", ylab="Global Active Power (kilowatts)", xlab="")
+     lines(Sub_metering_2~Datetime,col='Red')
+     lines(Sub_metering_3~Datetime,col='Blue')
+ })
> legend("topright", col=c("black", "red", "blue"), lty=1, lwd=2, legend=c("Sub_metering_1", "Sub_metering_2", "Sub_metering_3"))
> par(mfrow=c(2,2), mar=c(4,4,2,1), oma=c(0,0,2,0))
> 
> with(data, {
+     plot(Global_active_power~Datetime, type="l", ylab="Global Active Power (kilowatts)", xlab="")
+     plot(Voltage~Datetime, type="l", ylab="Voltage (volt)", xlab="")
+     plot(Sub_metering_1~Datetime, type="l", ylab="Global Active Power (kilowatts)", xlab="")
+     lines(Sub_metering_2~Datetime,col='Red')
+     lines(Sub_metering_3~Datetime,col='Blue')
+     legend("topright", col=c("black", "red", "blue"), lty=1, lwd=2, bty="n",legend=c("Sub_metering_1", "Sub_metering_2", "Sub_metering_3"))
+     plot(Global_reactive_power~Datetime, type="l", ylab="Global Rective Power (kilowatts)",xlab="")
+ })
> setwd("C:/Users/ASUS/Desktop/R software/exdata_data_household_power_consumption")
> > data_power <- read.csv("household_power_consumption.txt", header=TRUE, sep=';',nrows=2075259, na.strings="?", 
Error: unexpected '>' in ">"
> setwd("C:/Users/ASUS/Desktop/R software/exdata_data_household_power_consumption")
> data_power <- read.csv("household_power_consumption.txt", header=TRUE, sep=';',nrows=2075259, na.strings="?", 
+                          +                        check.names=F, stringsAsFactors=FALSE, comment.char="", quote='\"')
Error: unexpected '=' in:
"data_power <- read.csv("household_power_consumption.txt", header=TRUE, sep=';',nrows=2075259, na.strings="?", 
                         +                        check.names="
> View(data)
> View(data)
