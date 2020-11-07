---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A05B39BF-87EB-471E-9FCD-F7807CB46B4D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1aa7cff6d655bf33fa1a317516fda20237f6fc14
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946038"
---
# <span data-ttu-id="c55a7-101">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c55a7-101">Set-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="c55a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c55a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c55a7-103">Configura a extensão de diagnóstico do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c55a7-103">Configures the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="c55a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c55a7-104">SYNTAX</span></span>

### <span data-ttu-id="c55a7-105">SetDiagnosticsExtension (padrão)</span><span class="sxs-lookup"><span data-stu-id="c55a7-105">SetDiagnosticsExtension (Default)</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c55a7-106">SetDiagnosticsWithReferenceExtension</span><span class="sxs-lookup"><span data-stu-id="c55a7-106">SetDiagnosticsWithReferenceExtension</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c55a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c55a7-107">DESCRIPTION</span></span>
<span data-ttu-id="c55a7-108">O cmdlet **set-AzureVMDiagnosticsExtension** configura a extensão de diagnóstico do Microsoft Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c55a7-108">The **Set-AzureVMDiagnosticsExtension** cmdlet configures the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="c55a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c55a7-109">EXAMPLES</span></span>

### <span data-ttu-id="c55a7-110">Exemplo 1: criar uma máquina virtual com a extensão de diagnóstico do Azure aplicada</span><span class="sxs-lookup"><span data-stu-id="c55a7-110">Example 1: Create a virtual machine with Azure Diagnostics extension applied</span></span>
```
PS C:\> $VM = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $VMImage
PS C:\> $VM = Add-AzureProvisioningConfig -VM $VM -AdminUsername $Username -Password $Password -Windows
PS C:\> $VM = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> New-AzureVM -Location $Location -ServiceName $Service_Name -VM $VM
```

<span data-ttu-id="c55a7-111">Esses comandos habilitam a extensão do diagnóstico do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c55a7-111">These commands enable the Azure Diagnostics extension on a virtual machine.</span></span>

### <span data-ttu-id="c55a7-112">Exemplo 2: habilitar uma extensão de diagnóstico do Azure em uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="c55a7-112">Example 2: Enable an Azure Diagnostics extension on an existing virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName $Service_Name -Name $VM_Name
PS C:\> $VM_Update = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> Update-AzureVM -ServiceName $Service_Name -Name $VM_Name -VM $VM_Update.VM
```

<span data-ttu-id="c55a7-113">O primeiro comando usa o cmdlet **Get-AzureVM** para obter uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c55a7-113">The first command uses the **Get-AzureVM** cmdlet to get a virtual machine.</span></span>

<span data-ttu-id="c55a7-114">O segundo comando usa o cmdlet **set-AzureVMDiagnosticsExtension** para atualizar a configuração da máquina virtual para incluir a extensão do diagnóstico do Azure.</span><span class="sxs-lookup"><span data-stu-id="c55a7-114">The second command uses the **Set-AzureVMDiagnosticsExtension** cmdlet to update the virtual machine configuration to include the Azure Diagnostics extension.</span></span>

<span data-ttu-id="c55a7-115">O comando final aplica a configuração atualizada à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c55a7-115">The final command applies the updated configuration to the virtual machine.</span></span>

## <span data-ttu-id="c55a7-116">OS</span><span class="sxs-lookup"><span data-stu-id="c55a7-116">PARAMETERS</span></span>

### <span data-ttu-id="c55a7-117">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="c55a7-117">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="c55a7-118">Especifica um caminho para a configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="c55a7-118">Specifies a path for the diagnostics configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55a7-119">-Disable</span><span class="sxs-lookup"><span data-stu-id="c55a7-119">-Disable</span></span>
<span data-ttu-id="c55a7-120">Indica que esse cmdlet desabilita a extensão do diagnóstico na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c55a7-120">Indicates that this cmdlet disables the diagnostics extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c55a7-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="c55a7-121">-InformationAction</span></span>
<span data-ttu-id="c55a7-122">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="c55a7-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c55a7-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c55a7-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c55a7-124">Contínuo</span><span class="sxs-lookup"><span data-stu-id="c55a7-124">Continue</span></span>
- <span data-ttu-id="c55a7-125">Ignorar</span><span class="sxs-lookup"><span data-stu-id="c55a7-125">Ignore</span></span>
- <span data-ttu-id="c55a7-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="c55a7-126">Inquire</span></span>
- <span data-ttu-id="c55a7-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c55a7-127">SilentlyContinue</span></span>
- <span data-ttu-id="c55a7-128">Finaliza</span><span class="sxs-lookup"><span data-stu-id="c55a7-128">Stop</span></span>
- <span data-ttu-id="c55a7-129">Suspensão</span><span class="sxs-lookup"><span data-stu-id="c55a7-129">Suspend</span></span>

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

### <span data-ttu-id="c55a7-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c55a7-130">-InformationVariable</span></span>
<span data-ttu-id="c55a7-131">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="c55a7-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c55a7-132">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c55a7-132">-Profile</span></span>
<span data-ttu-id="c55a7-133">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c55a7-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c55a7-134">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c55a7-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c55a7-135">-Referencename</span><span class="sxs-lookup"><span data-stu-id="c55a7-135">-ReferenceName</span></span>
<span data-ttu-id="c55a7-136">Especifica o nome de referência para a extensão do diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="c55a7-136">Specifies the reference name for the diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: SetDiagnosticsWithReferenceExtension
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c55a7-137">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="c55a7-137">-StorageAccountEndpoint</span></span>
<span data-ttu-id="c55a7-138">Especifica um ponto de extremidade da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c55a7-138">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c55a7-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c55a7-139">-StorageAccountKey</span></span>
<span data-ttu-id="c55a7-140">Especifica uma chave de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c55a7-140">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c55a7-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c55a7-141">-StorageAccountName</span></span>
<span data-ttu-id="c55a7-142">Especifica um nome de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c55a7-142">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="c55a7-143">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="c55a7-143">-StorageContext</span></span>
<span data-ttu-id="c55a7-144">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c55a7-144">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c55a7-145">-Versão</span><span class="sxs-lookup"><span data-stu-id="c55a7-145">-Version</span></span>
<span data-ttu-id="c55a7-146">Especifica a versão de extensão como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c55a7-146">Specifies the extension version as a string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55a7-147">-VM</span><span class="sxs-lookup"><span data-stu-id="c55a7-147">-VM</span></span>
<span data-ttu-id="c55a7-148">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="c55a7-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="c55a7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c55a7-149">CommonParameters</span></span>
<span data-ttu-id="c55a7-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c55a7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c55a7-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c55a7-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c55a7-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c55a7-152">INPUTS</span></span>

## <span data-ttu-id="c55a7-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c55a7-153">OUTPUTS</span></span>

## <span data-ttu-id="c55a7-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c55a7-154">NOTES</span></span>

## <span data-ttu-id="c55a7-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c55a7-155">RELATED LINKS</span></span>

[<span data-ttu-id="c55a7-156">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c55a7-156">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="c55a7-157">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c55a7-157">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="c55a7-158">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c55a7-158">Update-AzureVM</span></span>](./Update-AzureVM.md)


