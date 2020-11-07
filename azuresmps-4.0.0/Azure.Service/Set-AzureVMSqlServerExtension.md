---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 56C7B6F5-C2AC-4C5A-8930-645374694CC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 053bb1bfb31b90a91d69e50b77ac6411321014f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945790"
---
# <span data-ttu-id="f1114-101">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f1114-101">Set-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="f1114-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1114-102">SYNOPSIS</span></span>
<span data-ttu-id="f1114-103">Define a extensão do SQL Server do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f1114-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="f1114-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1114-104">SYNTAX</span></span>

### <span data-ttu-id="f1114-105">EnableSqlServerExtension (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1114-105">EnableSqlServerExtension (Default)</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>]
 [[-AutoPatchingSettings] <AutoPatchingSettings>] [[-AutoBackupSettings] <AutoBackupSettings>]
 [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f1114-106">DisableSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f1114-106">DisableSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1114-107">UninstallSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f1114-107">UninstallSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f1114-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1114-108">DESCRIPTION</span></span>
<span data-ttu-id="f1114-109">O cmdlet **set-AzureVMSqlServerExtension** define a extensão do SQL Server do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f1114-109">The **Set-AzureVMSqlServerExtension** cmdlet sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="f1114-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1114-110">EXAMPLES</span></span>

### <span data-ttu-id="f1114-111">Exemplo 1: definir as configurações de correção automática em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="f1114-111">Example 1: Set auto-patching settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoPatchingSettings $APS | Update-AzureVM
```

<span data-ttu-id="f1114-112">Este comando define as configurações de correção automática em uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1114-112">This command sets auto-patching settings on an Azure virtual machine.</span></span>

### <span data-ttu-id="f1114-113">Exemplo 2: definir as configurações de backup automático em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="f1114-113">Example 2: Set auto-backup settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoBackupSettings $ABS | Update-AzureVM
```

<span data-ttu-id="f1114-114">Este comando define as configurações de backup automático na máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1114-114">This command sets auto-backup settings on Azure virtual machine.</span></span>

### <span data-ttu-id="f1114-115">Exemplo 3: desabilitar uma extensão do SQL Server em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="f1114-115">Example 3: Disable an SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Disable
```

<span data-ttu-id="f1114-116">Esse comando desabilita a extensão da máquina virtual do SQL Server em uma determinada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f1114-116">This command disables SQL Server virtual machine extension on a given virtual machine.</span></span>

### <span data-ttu-id="f1114-117">Exemplo 4: desinstalar uma extensão do SQL Server em uma máquina virtual específica</span><span class="sxs-lookup"><span data-stu-id="f1114-117">Example 4: Uninstall an SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Uninstall
```

<span data-ttu-id="f1114-118">Esse comando desinstala uma extensão de máquina virtual do SQL Server na máquina virtual chamada VMName.</span><span class="sxs-lookup"><span data-stu-id="f1114-118">This command uninstalls a SQL Server virtual machine extension on the virtual machine named VMName.</span></span>

## <span data-ttu-id="f1114-119">OS</span><span class="sxs-lookup"><span data-stu-id="f1114-119">PARAMETERS</span></span>

### <span data-ttu-id="f1114-120">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="f1114-120">-AutoBackupSettings</span></span>
<span data-ttu-id="f1114-121">Especifica as configurações de backup automático do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f1114-121">Specifies the automatic SQL Server backup settings.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1114-122">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="f1114-122">-AutoPatchingSettings</span></span>
<span data-ttu-id="f1114-123">Especifica as configurações de correção automática do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f1114-123">Specifies the automatic SQL Server patching settings.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1114-124">-Disable</span><span class="sxs-lookup"><span data-stu-id="f1114-124">-Disable</span></span>
<span data-ttu-id="f1114-125">Indica que esse cmdlet desabilita o estado da extensão.</span><span class="sxs-lookup"><span data-stu-id="f1114-125">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1114-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f1114-126">-InformationAction</span></span>
<span data-ttu-id="f1114-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="f1114-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f1114-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f1114-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1114-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="f1114-129">Continue</span></span>
- <span data-ttu-id="f1114-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="f1114-130">Ignore</span></span>
- <span data-ttu-id="f1114-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="f1114-131">Inquire</span></span>
- <span data-ttu-id="f1114-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f1114-132">SilentlyContinue</span></span>
- <span data-ttu-id="f1114-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="f1114-133">Stop</span></span>
- <span data-ttu-id="f1114-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="f1114-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1114-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f1114-135">-InformationVariable</span></span>
<span data-ttu-id="f1114-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="f1114-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1114-137">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="f1114-137">-KeyVaultCredentialSettings</span></span>
<span data-ttu-id="f1114-138">Especifica as configurações de credenciais do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f1114-138">Specifies key vault credential settings.</span></span>

```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1114-139">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f1114-139">-Profile</span></span>
<span data-ttu-id="f1114-140">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f1114-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f1114-141">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f1114-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1114-142">-Referencename</span><span class="sxs-lookup"><span data-stu-id="f1114-142">-ReferenceName</span></span>
<span data-ttu-id="f1114-143">Especifica o nome de referência da extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f1114-143">Specifies the reference name of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1114-144">-Desinstalar</span><span class="sxs-lookup"><span data-stu-id="f1114-144">-Uninstall</span></span>
<span data-ttu-id="f1114-145">Indica que esse cmdlet desinstala a extensão do SQL Server da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f1114-145">Indicates that this cmdlet uninstalls the SQL Server extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1114-146">-Versão</span><span class="sxs-lookup"><span data-stu-id="f1114-146">-Version</span></span>
<span data-ttu-id="f1114-147">Especifica a versão da extensão do SQL Server da qual Get-AzureVMSqlServerExtension recupera as configurações.</span><span class="sxs-lookup"><span data-stu-id="f1114-147">Specifies the version of the SQL Server extension that Get-AzureVMSqlServerExtension retrieves settings from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1114-148">-VM</span><span class="sxs-lookup"><span data-stu-id="f1114-148">-VM</span></span>
<span data-ttu-id="f1114-149">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="f1114-149">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1114-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1114-150">CommonParameters</span></span>
<span data-ttu-id="f1114-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1114-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1114-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1114-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1114-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1114-153">INPUTS</span></span>

## <span data-ttu-id="f1114-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1114-154">OUTPUTS</span></span>

## <span data-ttu-id="f1114-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1114-155">NOTES</span></span>

## <span data-ttu-id="f1114-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1114-156">RELATED LINKS</span></span>

[<span data-ttu-id="f1114-157">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f1114-157">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="f1114-158">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f1114-158">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)


