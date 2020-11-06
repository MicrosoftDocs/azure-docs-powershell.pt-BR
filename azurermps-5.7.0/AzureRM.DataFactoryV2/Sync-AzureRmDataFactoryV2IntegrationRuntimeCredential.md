---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/sync-azurermdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 11619cf9d5699b626032f82efbc9674713076ece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429831"
---
# <span data-ttu-id="2f9d7-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="2f9d7-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="2f9d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f9d7-102">SYNOPSIS</span></span>
<span data-ttu-id="2f9d7-103">Sincroniza as credenciais entre nós do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f9d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f9d7-104">SYNTAX</span></span>

### <span data-ttu-id="2f9d7-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f9d7-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f9d7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f9d7-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f9d7-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2f9d7-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f9d7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f9d7-108">DESCRIPTION</span></span>
<span data-ttu-id="2f9d7-109">O cmdlet **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** sincroniza as credenciais locais entre nós do tempo de execução de integração, o que obriga as credenciais a serem idênticas em todos os nós.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="2f9d7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f9d7-110">EXAMPLES</span></span>

### <span data-ttu-id="2f9d7-111">Exemplo 1: sincronizar uma credencial de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="2f9d7-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="2f9d7-112">O cmdlet sincroniza credenciais entre nós do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="2f9d7-113">OS</span><span class="sxs-lookup"><span data-stu-id="2f9d7-113">PARAMETERS</span></span>

### <span data-ttu-id="2f9d7-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2f9d7-114">-DataFactoryName</span></span>
<span data-ttu-id="2f9d7-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-115">The data factory name.</span></span>

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

### <span data-ttu-id="2f9d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f9d7-116">-DefaultProfile</span></span>
<span data-ttu-id="2f9d7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f9d7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2f9d7-118">-Force</span></span>
<span data-ttu-id="2f9d7-119">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2f9d7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f9d7-120">-InputObject</span></span>
<span data-ttu-id="2f9d7-121">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="2f9d7-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="2f9d7-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="2f9d7-123">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="2f9d7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f9d7-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f9d7-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-125">The resource group name.</span></span>

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

### <span data-ttu-id="2f9d7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f9d7-126">-ResourceId</span></span>
<span data-ttu-id="2f9d7-127">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2f9d7-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2f9d7-128">-Confirm</span></span>
<span data-ttu-id="2f9d7-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f9d7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f9d7-130">-WhatIf</span></span>
<span data-ttu-id="2f9d7-131">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2f9d7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f9d7-132">CommonParameters</span></span>
<span data-ttu-id="2f9d7-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f9d7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f9d7-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f9d7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f9d7-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f9d7-135">INPUTS</span></span>

### <span data-ttu-id="2f9d7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2f9d7-136">System.String</span></span>
<span data-ttu-id="2f9d7-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2f9d7-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2f9d7-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f9d7-138">OUTPUTS</span></span>

### <span data-ttu-id="2f9d7-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="2f9d7-139">System.Object</span></span>

## <span data-ttu-id="2f9d7-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f9d7-140">NOTES</span></span>

## <span data-ttu-id="2f9d7-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f9d7-141">RELATED LINKS</span></span>

