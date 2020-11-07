---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948390"
---
# <span data-ttu-id="321ce-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="321ce-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="321ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="321ce-102">SYNOPSIS</span></span>
<span data-ttu-id="321ce-103">Define a extensão do SQL Server do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="321ce-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="321ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="321ce-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="321ce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="321ce-105">DESCRIPTION</span></span>
<span data-ttu-id="321ce-106">O cmdlet **set-AzVMSqlServerExtension** define a extensão do servidor AzureSQL em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="321ce-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="321ce-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="321ce-107">EXAMPLES</span></span>

### <span data-ttu-id="321ce-108">Exemplo 1: definir as configurações de correção automática em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="321ce-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="321ce-109">O primeiro comando cria um objeto de configuração usando o cmdlet **New-AzVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="321ce-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="321ce-110">O comando armazena a configuração na variável $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="321ce-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="321ce-111">O segundo comando obtém a máquina virtual chamada VirtualMachine11 no serviço chamado Service02 usando o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="321ce-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="321ce-112">O comando passa o objeto para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="321ce-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="321ce-113">O cmdlet atual define as configurações de correção automática em $AutoPatchingConfig para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="321ce-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="321ce-114">O comando passa a máquina virtual para o cmdlet Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="321ce-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="321ce-115">Exemplo 2: definir configurações de backup automático em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="321ce-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="321ce-116">O primeiro comando cria um objeto de configuração usando o cmdlet **New-AzVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="321ce-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="321ce-117">O comando armazena a configuração na variável $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="321ce-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="321ce-118">O segundo comando obtém a máquina virtual chamada VirtualMachine11 no serviço chamado Service02 e, em seguida, a transmite para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="321ce-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="321ce-119">O cmdlet atual define as configurações de backup automático em $AutoBackupConfig para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="321ce-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="321ce-120">O comando passa a máquina virtual para o cmdlet Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="321ce-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="321ce-121">Exemplo 3: desabilitar uma extensão do SQL Server em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="321ce-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="321ce-122">Esse comando obtém uma máquina virtual chamada VirtualMachine08 no Service03 e, em seguida, a transmite para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="321ce-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="321ce-123">O comando desabilita a extensão da máquina virtual do SQL Server nessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="321ce-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="321ce-124">Exemplo 4: desinstalar uma extensão do SQL Server em uma máquina virtual específica</span><span class="sxs-lookup"><span data-stu-id="321ce-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="321ce-125">Esse comando obtém uma máquina virtual chamada VirtualMachine08 no Service03 e, em seguida, a transmite para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="321ce-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="321ce-126">O comando desinstala uma extensão de máquina virtual do SQL Server nessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="321ce-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="321ce-127">OS</span><span class="sxs-lookup"><span data-stu-id="321ce-127">PARAMETERS</span></span>

### <span data-ttu-id="321ce-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="321ce-128">-AutoBackupSettings</span></span>
<span data-ttu-id="321ce-129">Especifica as configurações de backup automático do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="321ce-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="321ce-130">Para criar um objeto **AutoBackupSettings** , use o cmdlet New-AzVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="321ce-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="321ce-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="321ce-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="321ce-132">Especifica as configurações de correção automática do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="321ce-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="321ce-133">Para criar um objeto **AutoPatchingSettings** , use o cmdlet New-AzVMSqlServerAutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="321ce-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="321ce-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="321ce-134">-DefaultProfile</span></span>
<span data-ttu-id="321ce-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="321ce-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="321ce-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="321ce-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="321ce-137">-Local</span><span class="sxs-lookup"><span data-stu-id="321ce-137">-Location</span></span>
<span data-ttu-id="321ce-138">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="321ce-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="321ce-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="321ce-139">-Name</span></span>
<span data-ttu-id="321ce-140">Especifica o nome do SQL Server a extensão.</span><span class="sxs-lookup"><span data-stu-id="321ce-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="321ce-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="321ce-141">-ResourceGroupName</span></span>
<span data-ttu-id="321ce-142">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="321ce-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="321ce-143">-Versão</span><span class="sxs-lookup"><span data-stu-id="321ce-143">-Version</span></span>
<span data-ttu-id="321ce-144">Especifica a versão da extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="321ce-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="321ce-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="321ce-145">-VMName</span></span>
<span data-ttu-id="321ce-146">Especifica o nome da máquina virtual na qual esse cmdlet define a extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="321ce-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="321ce-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="321ce-147">CommonParameters</span></span>
<span data-ttu-id="321ce-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="321ce-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="321ce-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="321ce-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="321ce-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="321ce-150">INPUTS</span></span>

### <span data-ttu-id="321ce-151">System. String</span><span class="sxs-lookup"><span data-stu-id="321ce-151">System.String</span></span>

### <span data-ttu-id="321ce-152">Microsoft. Azure. Commands. COMPUTE. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="321ce-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="321ce-153">Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="321ce-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="321ce-154">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="321ce-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="321ce-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="321ce-155">OUTPUTS</span></span>

### <span data-ttu-id="321ce-156">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="321ce-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="321ce-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="321ce-157">NOTES</span></span>

## <span data-ttu-id="321ce-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="321ce-158">RELATED LINKS</span></span>

[<span data-ttu-id="321ce-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="321ce-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="321ce-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="321ce-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="321ce-161">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="321ce-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="321ce-162">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="321ce-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="321ce-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="321ce-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="321ce-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="321ce-164">Update-AzVM</span></span>](./Update-AzVM.md)


