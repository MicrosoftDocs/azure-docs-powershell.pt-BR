---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 63889ce74af1051211a579d1af7cc54be14822f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602225"
---
# <span data-ttu-id="d31f9-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="d31f9-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="d31f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d31f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d31f9-103">Sincroniza as credenciais entre nós do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="d31f9-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d31f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d31f9-104">SYNTAX</span></span>

### <span data-ttu-id="d31f9-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d31f9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d31f9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d31f9-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d31f9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d31f9-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d31f9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d31f9-108">DESCRIPTION</span></span>
<span data-ttu-id="d31f9-109">O cmdlet **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** sincroniza as credenciais locais entre nós do tempo de execução de integração, o que obriga as credenciais a serem idênticas em todos os nós.</span><span class="sxs-lookup"><span data-stu-id="d31f9-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="d31f9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d31f9-110">EXAMPLES</span></span>

### <span data-ttu-id="d31f9-111">Exemplo 1: sincronizar uma credencial de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="d31f9-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="d31f9-112">O cmdlet sincroniza credenciais entre nós do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="d31f9-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="d31f9-113">OS</span><span class="sxs-lookup"><span data-stu-id="d31f9-113">PARAMETERS</span></span>

### <span data-ttu-id="d31f9-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d31f9-114">-Confirm</span></span>
<span data-ttu-id="d31f9-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d31f9-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31f9-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d31f9-116">-DataFactoryName</span></span>
<span data-ttu-id="d31f9-117">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="d31f9-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31f9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d31f9-118">-Force</span></span>
<span data-ttu-id="d31f9-119">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="d31f9-119">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31f9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d31f9-120">-InputObject</span></span>
<span data-ttu-id="d31f9-121">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="d31f9-121">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d31f9-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="d31f9-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="d31f9-123">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="d31f9-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31f9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d31f9-124">-ResourceGroupName</span></span>
<span data-ttu-id="d31f9-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d31f9-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31f9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d31f9-126">-ResourceId</span></span>
<span data-ttu-id="d31f9-127">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="d31f9-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31f9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d31f9-128">-WhatIf</span></span>
<span data-ttu-id="d31f9-129">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d31f9-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="d31f9-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d31f9-130">INPUTS</span></span>

### <span data-ttu-id="d31f9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d31f9-131">System.String</span></span>
<span data-ttu-id="d31f9-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d31f9-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="d31f9-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d31f9-133">OUTPUTS</span></span>

### <span data-ttu-id="d31f9-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="d31f9-134">System.Object</span></span>

## <span data-ttu-id="d31f9-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d31f9-135">NOTES</span></span>

## <span data-ttu-id="d31f9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d31f9-136">RELATED LINKS</span></span>
