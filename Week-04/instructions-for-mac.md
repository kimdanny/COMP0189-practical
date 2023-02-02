# Instructions for Mac Users

## (Necessary step) Disable Mac's Malware check 
Since SPM12 and PRoNTo is downloaded from external developer, you will see many warning messages like "Application cannot be opened because the developer cannot be verified". This stops you from running PRoNTo.

To disable the security check, 
1. Type the following in your terminal
    ```bash
    $ sudo spctl --master-disable
    ```

2. Open System Preferences > Security & Privacy

3. In the General tab, selet 'Anywhere' button under the "Allow apps downloaded from:" question.

**You can always turn the security check on by**:
```bash
$ sudo spctl --master-enable
```



## (potentially necessary steps) When you run into compiler problems
It is advised to do the following steps in case there is an issue with your Mac version.
Xcode is a compiler with which we compile C/C++ code (which is found in some external libraries used by PRoNTo) to `.mex` files, which is a file that MATLAB can use to run C/C++ code. 
There can be an older `.mex` file version already compiled within the libraries if you have old version of Mac. 
However, there can always be an issue with some of the Mac versions, in which case you will have to do all the following instructions.

### 1. Download `Xcode`
You can download Xcode from App Store.
Xcode is a heavy application, so make sure you download it before the practical session.

### 2. Install Xcode Command Line Tools
```bash
$ xcode-select --install
```

### 3. Activate Compilers
It's common to run into problems when using `mex` in MATLAB.
Troubleshoot with [this website](https://uk.mathworks.com/matlabcentral/answers/470698-error-using-mex-no-supported-compiler-was-found-on-mac?s_tid=prof_contriblnk).  

```bash
$ sudo xcode-select -s /Applications/Xcode.app/Contents/Developer

$ sudo xcodebuild -license accept
```


