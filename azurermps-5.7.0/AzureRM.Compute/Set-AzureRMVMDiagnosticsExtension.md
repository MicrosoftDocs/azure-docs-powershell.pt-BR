---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: d93fd01fb178f093b6ed5527cca0c018cebe4f16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431712"
---
# <span data-ttu-id="1cba2-101">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1cba2-101">Set-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="1cba2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cba2-102">SYNOPSIS</span></span>
<span data-ttu-id="1cba2-103">Configura a extensão de diagnóstico do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1cba2-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cba2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cba2-104">SYNTAX</span></span>

```
Set-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [<CommonParameters>]
```

## <span data-ttu-id="1cba2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cba2-105">DESCRIPTION</span></span>
<span data-ttu-id="1cba2-106">O cmdlet **set-AzureRmVMDiagnosticsExtension** configura a extensão de diagnóstico do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1cba2-106">The **Set-AzureRmVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="1cba2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cba2-107">EXAMPLES</span></span>

### <span data-ttu-id="1cba2-108">Exemplo 1: habilitar o diagnóstico usando uma conta de armazenamento especificada em um arquivo de configuração de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="1cba2-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="1cba2-109">Esse comando usa um arquivo de configuração de diagnóstico para habilitar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="1cba2-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="1cba2-110">O arquivo diagnostics_publicconfig.xml contém a configuração de XML público para a extensão do diagnóstico, incluindo o nome da conta de armazenamento à qual os dados de diagnóstico serão enviados.</span><span class="sxs-lookup"><span data-stu-id="1cba2-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="1cba2-111">A conta de armazenamento de diagnóstico deve estar na mesma assinatura que a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1cba2-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="1cba2-112">Exemplo 2: habilitar o diagnóstico usando um nome de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1cba2-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="1cba2-113">Esse comando usa o nome da conta de armazenamento para habilitar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="1cba2-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="1cba2-114">Se a configuração de diagnóstico não especificar um nome de conta de armazenamento ou se você quiser substituir o nome da conta de armazenamento de diagnóstico especificado no arquivo de configuração, use o parâmetro *StorageAccountName* .</span><span class="sxs-lookup"><span data-stu-id="1cba2-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="1cba2-115">A conta de armazenamento de diagnóstico deve estar na mesma assinatura que a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1cba2-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="1cba2-116">Exemplo 3: habilitar o diagnóstico usando o nome e a chave da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1cba2-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="1cba2-117">Esse comando usa o nome da conta de armazenamento e a chave para habilitar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="1cba2-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="1cba2-118">Se a conta de armazenamento de diagnóstico estiver em uma assinatura diferente da máquina virtual, então habilite o envio de dados de diagnóstico para essa conta de armazenamento especificando explicitamente seu nome e chave.</span><span class="sxs-lookup"><span data-stu-id="1cba2-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="1cba2-119">OS</span><span class="sxs-lookup"><span data-stu-id="1cba2-119">PARAMETERS</span></span>

### <span data-ttu-id="1cba2-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1cba2-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1cba2-121">Indica se esse cmdlet permite que o agente convidado do Azure atualize automaticamente a extensão para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="1cba2-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cba2-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="1cba2-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="1cba2-123">Especifica o caminho do arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="1cba2-123">Specifies the path of the configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cba2-124">-Local</span><span class="sxs-lookup"><span data-stu-id="1cba2-124">-Location</span></span>
<span data-ttu-id="1cba2-125">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1cba2-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cba2-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="1cba2-126">-Name</span></span>
<span data-ttu-id="1cba2-127">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="1cba2-127">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cba2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cba2-128">-ResourceGroupName</span></span>
<span data-ttu-id="1cba2-129">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1cba2-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cba2-130">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="1cba2-130">-StorageAccountEndpoint</span></span>
<span data-ttu-id="1cba2-131">Especifica o ponto de extremidade da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1cba2-131">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cba2-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1cba2-132">-StorageAccountKey</span></span>
<span data-ttu-id="1cba2-133">Especifica a chave da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1cba2-133">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cba2-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1cba2-134">-StorageAccountName</span></span>
<span data-ttu-id="1cba2-135">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1cba2-135">Specifies the storage account name.</span></span>

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

### <span data-ttu-id="1cba2-136">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="1cba2-136">-StorageContext</span></span>
<span data-ttu-id="1cba2-137">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cba2-137">Specifies the Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cba2-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1cba2-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="1cba2-139">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1cba2-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="1cba2-140">Para obter a versão, execute o cmdlet Get-AzureRmVMExtensionImage com um valor de Microsoft. COMPUTE para o parâmetro *PublisherName* e VMAccessAgent para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="1cba2-140">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cba2-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="1cba2-141">-VMName</span></span>
<span data-ttu-id="1cba2-142">Especifica o nome da máquina virtual na qual esse cmdlet funciona.</span><span class="sxs-lookup"><span data-stu-id="1cba2-142">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cba2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cba2-143">CommonParameters</span></span>
<span data-ttu-id="1cba2-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cba2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cba2-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cba2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cba2-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cba2-146">INPUTS</span></span>

### <span data-ttu-id="1cba2-147">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1cba2-147">None</span></span>
<span data-ttu-id="1cba2-148">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1cba2-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1cba2-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cba2-149">OUTPUTS</span></span>

## <span data-ttu-id="1cba2-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cba2-150">NOTES</span></span>

## <span data-ttu-id="1cba2-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cba2-151">RELATED LINKS</span></span>

[<span data-ttu-id="1cba2-152">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1cba2-152">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="1cba2-153">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1cba2-153">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="1cba2-154">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1cba2-154">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)


