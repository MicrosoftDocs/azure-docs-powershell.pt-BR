---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: 96651a495f08657a4cd9006545cfa104285ec7ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116902"
---
# <span data-ttu-id="debfc-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="debfc-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="debfc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="debfc-102">SYNOPSIS</span></span>
<span data-ttu-id="debfc-103">Criar um objeto na memória para a Extensão de Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="debfc-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="debfc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="debfc-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="debfc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="debfc-105">DESCRIPTION</span></span>
<span data-ttu-id="debfc-106">Criar um objeto na memória para a Extensão de Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="debfc-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="debfc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="debfc-107">EXAMPLES</span></span>

### <span data-ttu-id="debfc-108">Exemplo 1: Criar objeto de extensão de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="debfc-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="debfc-109">Esse comando cria um objeto de extensão de diagnóstico que é usado para criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="debfc-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="debfc-110">Para obter mais detalhes, consulte New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="debfc-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="debfc-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="debfc-111">PARAMETERS</span></span>

### <span data-ttu-id="debfc-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="debfc-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="debfc-113">Atualizar automaticamente a versão secundária.</span><span class="sxs-lookup"><span data-stu-id="debfc-113">Auto upgrade minor version.</span></span>

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

### <span data-ttu-id="debfc-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="debfc-114">-CloudServiceName</span></span>
<span data-ttu-id="debfc-115">Nome do Serviço de Nuvem.</span><span class="sxs-lookup"><span data-stu-id="debfc-115">Name of Cloud Service.</span></span>

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

### <span data-ttu-id="debfc-116">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="debfc-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="debfc-117">Especifica a configuração do Diagnóstico do Azure.</span><span class="sxs-lookup"><span data-stu-id="debfc-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="debfc-118">Você pode baixar o esquema usando o seguinte comando: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics'). PublicConfigurationSchema | Out-File -Codificação utf8 -FilePath 'PigConfig.xsd'</span><span class="sxs-lookup"><span data-stu-id="debfc-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

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

### <span data-ttu-id="debfc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="debfc-119">-Name</span></span>
<span data-ttu-id="debfc-120">Nome da Extensão de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="debfc-120">Name of Diagnostics Extension.</span></span>

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

### <span data-ttu-id="debfc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="debfc-121">-ResourceGroupName</span></span>
<span data-ttu-id="debfc-122">Nome do Grupo de Recursos do Serviço na Nuvem.</span><span class="sxs-lookup"><span data-stu-id="debfc-122">Resource Group name of Cloud Service.</span></span>

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

### <span data-ttu-id="debfc-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="debfc-123">-RolesAppliedTo</span></span>
<span data-ttu-id="debfc-124">Funções aplicadas a.</span><span class="sxs-lookup"><span data-stu-id="debfc-124">Roles applied to.</span></span>

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

### <span data-ttu-id="debfc-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="debfc-125">-StorageAccountKey</span></span>
<span data-ttu-id="debfc-126">Chave da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="debfc-126">Storage Account Key.</span></span>

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

### <span data-ttu-id="debfc-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="debfc-127">-StorageAccountName</span></span>
<span data-ttu-id="debfc-128">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="debfc-128">Name of the Storage Account.</span></span>

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

### <span data-ttu-id="debfc-129">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="debfc-129">-Subscription</span></span>
<span data-ttu-id="debfc-130">Assinatura.</span><span class="sxs-lookup"><span data-stu-id="debfc-130">Subscription.</span></span>

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

### <span data-ttu-id="debfc-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="debfc-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="debfc-132">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="debfc-132">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="debfc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debfc-133">CommonParameters</span></span>
<span data-ttu-id="debfc-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="debfc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debfc-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="debfc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debfc-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="debfc-136">INPUTS</span></span>

## <span data-ttu-id="debfc-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="debfc-137">OUTPUTS</span></span>

### <span data-ttu-id="debfc-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="debfc-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="debfc-139">Notas</span><span class="sxs-lookup"><span data-stu-id="debfc-139">NOTES</span></span>

<span data-ttu-id="debfc-140">Aliases</span><span class="sxs-lookup"><span data-stu-id="debfc-140">ALIASES</span></span>

## <span data-ttu-id="debfc-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="debfc-141">RELATED LINKS</span></span>

