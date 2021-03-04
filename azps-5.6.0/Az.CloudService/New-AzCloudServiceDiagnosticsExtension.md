---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: a87e9c76b2c083392fc37d74a3ba213dba5881ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887587"
---
# <span data-ttu-id="ed18d-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ed18d-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="ed18d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed18d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed18d-103">Criar um objeto na memória para a Extensão de Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="ed18d-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="ed18d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ed18d-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="ed18d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ed18d-105">DESCRIPTION</span></span>
<span data-ttu-id="ed18d-106">Criar um objeto na memória para a Extensão de Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="ed18d-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="ed18d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed18d-107">EXAMPLES</span></span>

### <span data-ttu-id="ed18d-108">Exemplo 1: Criar objeto de extensão de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="ed18d-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="ed18d-109">Este comando cria um objeto de extensão de diagnóstico que é usado para criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="ed18d-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="ed18d-110">Para obter mais detalhes, consulte New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="ed18d-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="ed18d-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ed18d-111">PARAMETERS</span></span>

### <span data-ttu-id="ed18d-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ed18d-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ed18d-113">Versão secundária de atualização automática.</span><span class="sxs-lookup"><span data-stu-id="ed18d-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed18d-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="ed18d-114">-CloudServiceName</span></span>
<span data-ttu-id="ed18d-115">Nome do Serviço de Nuvem.</span><span class="sxs-lookup"><span data-stu-id="ed18d-115">Name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed18d-116">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="ed18d-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="ed18d-117">Especifica a configuração do Diagnóstico do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed18d-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="ed18d-118">Você pode baixar o esquema usando o seguinte comando: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics'). PublicConfigurationSchema | Out-File -Codificação utf8 -FilePath 'WadConfig.xsd'</span><span class="sxs-lookup"><span data-stu-id="ed18d-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed18d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ed18d-119">-Name</span></span>
<span data-ttu-id="ed18d-120">Nome da Extensão de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="ed18d-120">Name of Diagnostics Extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed18d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed18d-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed18d-122">Nome do Grupo de Recursos do Serviço de Nuvem.</span><span class="sxs-lookup"><span data-stu-id="ed18d-122">Resource Group name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed18d-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="ed18d-123">-RolesAppliedTo</span></span>
<span data-ttu-id="ed18d-124">Funções aplicadas a.</span><span class="sxs-lookup"><span data-stu-id="ed18d-124">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed18d-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ed18d-125">-StorageAccountKey</span></span>
<span data-ttu-id="ed18d-126">Chave de Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ed18d-126">Storage Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed18d-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ed18d-127">-StorageAccountName</span></span>
<span data-ttu-id="ed18d-128">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ed18d-128">Name of the Storage Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed18d-129">-Subscription</span><span class="sxs-lookup"><span data-stu-id="ed18d-129">-Subscription</span></span>
<span data-ttu-id="ed18d-130">Assinatura.</span><span class="sxs-lookup"><span data-stu-id="ed18d-130">Subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed18d-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ed18d-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="ed18d-132">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="ed18d-132">Specifies the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed18d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed18d-133">CommonParameters</span></span>
<span data-ttu-id="ed18d-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed18d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed18d-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed18d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed18d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed18d-136">INPUTS</span></span>

## <span data-ttu-id="ed18d-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ed18d-137">OUTPUTS</span></span>

### <span data-ttu-id="ed18d-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="ed18d-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="ed18d-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="ed18d-139">NOTES</span></span>

<span data-ttu-id="ed18d-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ed18d-140">ALIASES</span></span>

## <span data-ttu-id="ed18d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed18d-141">RELATED LINKS</span></span>

