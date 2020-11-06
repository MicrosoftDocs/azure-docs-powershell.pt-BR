---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: a89a2fc342bf1a3ed6e311057f55bb83c80be210
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428263"
---
# <span data-ttu-id="b3d85-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b3d85-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="b3d85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3d85-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d85-103">Define a extensão do SQL Server do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3d85-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3d85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3d85-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3d85-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3d85-105">DESCRIPTION</span></span>
<span data-ttu-id="b3d85-106">O cmdlet **set-AzureRmVMSqlServerExtension** define a extensão do servidor AzureSQL em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3d85-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="b3d85-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3d85-107">EXAMPLES</span></span>

### <span data-ttu-id="b3d85-108">Exemplo 1: definir as configurações de correção automática em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="b3d85-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="b3d85-109">O primeiro comando cria um objeto de configuração usando o cmdlet **New-AzureVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="b3d85-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="b3d85-110">O comando armazena a configuração na variável $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="b3d85-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="b3d85-111">O segundo comando obtém a máquina virtual chamada VirtualMachine11 no serviço chamado Service02 usando o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="b3d85-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="b3d85-112">O comando passa o objeto para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="b3d85-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="b3d85-113">O cmdlet atual define as configurações de correção automática em $AutoPatchingConfig para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3d85-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="b3d85-114">O comando passa a máquina virtual para o cmdlet Update-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="b3d85-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="b3d85-115">Exemplo 2: definir configurações de backup automático em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="b3d85-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="b3d85-116">O primeiro comando cria um objeto de configuração usando o cmdlet **New-AzureVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="b3d85-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="b3d85-117">O comando armazena a configuração na variável $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="b3d85-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="b3d85-118">O segundo comando obtém a máquina virtual chamada VirtualMachine11 no serviço chamado Service02 e, em seguida, a transmite para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="b3d85-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="b3d85-119">O cmdlet atual define as configurações de backup automático em $AutoBackupConfig para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3d85-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="b3d85-120">O comando passa a máquina virtual para o cmdlet Update-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="b3d85-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="b3d85-121">Exemplo 3: desabilitar uma extensão do SQL Server em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="b3d85-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="b3d85-122">Esse comando obtém uma máquina virtual chamada VirtualMachine08 no Service03 e, em seguida, a transmite para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="b3d85-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b3d85-123">O comando desabilita a extensão da máquina virtual do SQL Server nessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3d85-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="b3d85-124">Exemplo 4: desinstalar uma extensão do SQL Server em uma máquina virtual específica</span><span class="sxs-lookup"><span data-stu-id="b3d85-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="b3d85-125">Esse comando obtém uma máquina virtual chamada VirtualMachine08 no Service03 e, em seguida, a transmite para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="b3d85-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b3d85-126">O comando desinstala uma extensão de máquina virtual do SQL Server nessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3d85-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="b3d85-127">OS</span><span class="sxs-lookup"><span data-stu-id="b3d85-127">PARAMETERS</span></span>

### <span data-ttu-id="b3d85-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="b3d85-128">-AutoBackupSettings</span></span>
<span data-ttu-id="b3d85-129">Especifica as configurações de backup automático do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b3d85-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="b3d85-130">Para criar um objeto **AutoBackupSettings** , use o cmdlet New-AzureVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="b3d85-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d85-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="b3d85-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="b3d85-132">Especifica as configurações de correção automática do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b3d85-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="b3d85-133">Para criar um objeto **AutoPatchingSettings** , use o cmdlet New-AzureVMSqlServerAutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="b3d85-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d85-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d85-134">-DefaultProfile</span></span>
<span data-ttu-id="b3d85-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3d85-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3d85-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="b3d85-136">-KeyVaultCredentialSettings</span></span>
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d85-137">-Local</span><span class="sxs-lookup"><span data-stu-id="b3d85-137">-Location</span></span>
<span data-ttu-id="b3d85-138">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3d85-138">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d85-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3d85-139">-Name</span></span>
<span data-ttu-id="b3d85-140">Especifica o nome do SQL Server a extensão.</span><span class="sxs-lookup"><span data-stu-id="b3d85-140">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d85-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d85-141">-ResourceGroupName</span></span>
<span data-ttu-id="b3d85-142">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3d85-142">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d85-143">-Versão</span><span class="sxs-lookup"><span data-stu-id="b3d85-143">-Version</span></span>
<span data-ttu-id="b3d85-144">Especifica a versão da extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b3d85-144">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d85-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="b3d85-145">-VMName</span></span>
<span data-ttu-id="b3d85-146">Especifica o nome da máquina virtual na qual esse cmdlet define a extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b3d85-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d85-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d85-147">CommonParameters</span></span>
<span data-ttu-id="b3d85-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d85-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d85-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3d85-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d85-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3d85-150">INPUTS</span></span>

## <span data-ttu-id="b3d85-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3d85-151">OUTPUTS</span></span>

## <span data-ttu-id="b3d85-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3d85-152">NOTES</span></span>

## <span data-ttu-id="b3d85-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3d85-153">RELATED LINKS</span></span>

[<span data-ttu-id="b3d85-154">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b3d85-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b3d85-155">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b3d85-155">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="b3d85-156">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="b3d85-156">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="b3d85-157">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="b3d85-157">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="b3d85-158">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b3d85-158">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="b3d85-159">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b3d85-159">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


