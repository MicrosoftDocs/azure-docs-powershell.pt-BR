---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 9aa895245f491e7b7ee077d083f052cd7e4e46e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889552"
---
# <span data-ttu-id="8d40e-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8d40e-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="8d40e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d40e-102">SYNOPSIS</span></span>
<span data-ttu-id="8d40e-103">Define a extensão do Azure SQL Server em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8d40e-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="8d40e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8d40e-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d40e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8d40e-105">DESCRIPTION</span></span>
<span data-ttu-id="8d40e-106">O cmdlet **Set-AzVMSqlServerExtension** define a extensão do Servidor do AzureSQL em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8d40e-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="8d40e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d40e-107">EXAMPLES</span></span>

### <span data-ttu-id="8d40e-108">Exemplo 1: Definir configurações de correção automática em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8d40e-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="8d40e-109">O primeiro comando cria um objeto de configuração usando o cmdlet **New-AzVMSqlServerAutoPatchingConfig.**</span><span class="sxs-lookup"><span data-stu-id="8d40e-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="8d40e-110">O comando armazena a configuração na $AutoPatchingConfig variável.</span><span class="sxs-lookup"><span data-stu-id="8d40e-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="8d40e-111">O segundo comando obtém a máquina virtual chamada VirtualMachine11 no serviço chamado Service02 usando o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8d40e-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="8d40e-112">O comando passa esse objeto para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="8d40e-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8d40e-113">O cmdlet atual define as configurações de correção automáticas $AutoPatchingConfig para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8d40e-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="8d40e-114">O comando passa a máquina virtual para o Update-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d40e-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="8d40e-115">Exemplo 2: Definir configurações de backup automático em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8d40e-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="8d40e-116">O primeiro comando cria um objeto de configuração usando o cmdlet **New-AzVMSqlServerAutoBackupConfig.**</span><span class="sxs-lookup"><span data-stu-id="8d40e-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="8d40e-117">O comando armazena a configuração na $AutoBackupConfig variável.</span><span class="sxs-lookup"><span data-stu-id="8d40e-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="8d40e-118">O segundo comando obtém a máquina virtual chamada VirtualMachine11 no serviço chamado Service02 e a passa para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="8d40e-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="8d40e-119">O cmdlet atual define as configurações de backup automáticas $AutoBackupConfig para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8d40e-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="8d40e-120">O comando passa a máquina virtual para o Update-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d40e-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="8d40e-121">Exemplo 3: Desabilitar uma extensão SQL Server em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8d40e-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="8d40e-122">Este comando obtém uma máquina virtual chamada VirtualMachine08 em Service03 e, em seguida, passa-a para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="8d40e-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="8d40e-123">O comando desabilita SQL Server de máquina virtual nessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8d40e-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="8d40e-124">Exemplo 4: Desinstale uma extensão SQL Server em uma máquina virtual específica</span><span class="sxs-lookup"><span data-stu-id="8d40e-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="8d40e-125">Este comando obtém uma máquina virtual chamada VirtualMachine08 em Service03 e, em seguida, passa-a para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="8d40e-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="8d40e-126">O comando desinstala uma extensão SQL Server máquina virtual nessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8d40e-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="8d40e-127">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8d40e-127">PARAMETERS</span></span>

### <span data-ttu-id="8d40e-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="8d40e-128">-AutoBackupSettings</span></span>
<span data-ttu-id="8d40e-129">Especifica as configurações automáticas SQL Server backup.</span><span class="sxs-lookup"><span data-stu-id="8d40e-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="8d40e-130">Para criar um **objeto AutoBackupSettings,** use New-AzVMSqlServerAutoBackupConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d40e-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="8d40e-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="8d40e-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="8d40e-132">Especifica as configurações de SQL Server de correção automáticas.</span><span class="sxs-lookup"><span data-stu-id="8d40e-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="8d40e-133">Para criar um **objeto AutoPatchingSettings,** use New-AzVMSqlServerAutoPatchingConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d40e-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="8d40e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d40e-134">-DefaultProfile</span></span>
<span data-ttu-id="8d40e-135">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8d40e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d40e-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="8d40e-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="8d40e-137">-Location</span><span class="sxs-lookup"><span data-stu-id="8d40e-137">-Location</span></span>
<span data-ttu-id="8d40e-138">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8d40e-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="8d40e-139">-Name</span><span class="sxs-lookup"><span data-stu-id="8d40e-139">-Name</span></span>
<span data-ttu-id="8d40e-140">Especifica o nome da SQL Server da extensão.</span><span class="sxs-lookup"><span data-stu-id="8d40e-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="8d40e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d40e-141">-ResourceGroupName</span></span>
<span data-ttu-id="8d40e-142">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8d40e-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8d40e-143">-Version</span><span class="sxs-lookup"><span data-stu-id="8d40e-143">-Version</span></span>
<span data-ttu-id="8d40e-144">Especifica a versão da extensão SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8d40e-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="8d40e-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="8d40e-145">-VMName</span></span>
<span data-ttu-id="8d40e-146">Especifica o nome da máquina virtual na qual este cmdlet define SQL Server extensão.</span><span class="sxs-lookup"><span data-stu-id="8d40e-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="8d40e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d40e-147">CommonParameters</span></span>
<span data-ttu-id="8d40e-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d40e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d40e-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d40e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d40e-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d40e-150">INPUTS</span></span>

### <span data-ttu-id="8d40e-151">System.String</span><span class="sxs-lookup"><span data-stu-id="8d40e-151">System.String</span></span>

### <span data-ttu-id="8d40e-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="8d40e-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="8d40e-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="8d40e-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="8d40e-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="8d40e-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="8d40e-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8d40e-155">OUTPUTS</span></span>

### <span data-ttu-id="8d40e-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8d40e-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8d40e-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="8d40e-157">NOTES</span></span>

## <span data-ttu-id="8d40e-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d40e-158">RELATED LINKS</span></span>

[<span data-ttu-id="8d40e-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8d40e-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8d40e-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8d40e-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="8d40e-161">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="8d40e-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="8d40e-162">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="8d40e-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="8d40e-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8d40e-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="8d40e-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8d40e-164">Update-AzVM</span></span>](./Update-AzVM.md)


