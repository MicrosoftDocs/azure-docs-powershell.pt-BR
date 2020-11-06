---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: ebea93e7d59e0740aa21e909f35779857aacba01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427818"
---
# <span data-ttu-id="3a52e-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3a52e-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="3a52e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a52e-102">SYNOPSIS</span></span>
<span data-ttu-id="3a52e-103">Atualiza uma pesquisa salva que já existe.</span><span class="sxs-lookup"><span data-stu-id="3a52e-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a52e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a52e-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tags] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a52e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a52e-105">DESCRIPTION</span></span>
<span data-ttu-id="3a52e-106">O cmdlet **set-AzureRmOperationalInsightsSavedSearch** atualiza uma pesquisa salva que já existe.</span><span class="sxs-lookup"><span data-stu-id="3a52e-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="3a52e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a52e-107">EXAMPLES</span></span>

### <span data-ttu-id="3a52e-108">Exemplo 1: define uma pesquisa salva com propriedades atualizadas</span><span class="sxs-lookup"><span data-stu-id="3a52e-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="3a52e-109">Este comando define uma pesquisa salva com propriedades atualizadas.</span><span class="sxs-lookup"><span data-stu-id="3a52e-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="3a52e-110">OS</span><span class="sxs-lookup"><span data-stu-id="3a52e-110">PARAMETERS</span></span>

### <span data-ttu-id="3a52e-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="3a52e-111">-Category</span></span>
<span data-ttu-id="3a52e-112">Especifica o nome da categoria.</span><span class="sxs-lookup"><span data-stu-id="3a52e-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a52e-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3a52e-113">-DisplayName</span></span>
<span data-ttu-id="3a52e-114">Especifica o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="3a52e-114">Specifies the display name.</span></span>

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

### <span data-ttu-id="3a52e-115">-ETag</span><span class="sxs-lookup"><span data-stu-id="3a52e-115">-ETag</span></span>
<span data-ttu-id="3a52e-116">Especifica o nome ETag.</span><span class="sxs-lookup"><span data-stu-id="3a52e-116">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="3a52e-117">-Consulta</span><span class="sxs-lookup"><span data-stu-id="3a52e-117">-Query</span></span>
<span data-ttu-id="3a52e-118">Especifica o nome da consulta.</span><span class="sxs-lookup"><span data-stu-id="3a52e-118">Specifies the query name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a52e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a52e-119">-ResourceGroupName</span></span>
<span data-ttu-id="3a52e-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a52e-120">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a52e-121">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="3a52e-121">-SavedSearchId</span></span>
<span data-ttu-id="3a52e-122">Especifica a ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="3a52e-122">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="3a52e-123">-Marcas</span><span class="sxs-lookup"><span data-stu-id="3a52e-123">-Tags</span></span>
```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a52e-124">-Versão</span><span class="sxs-lookup"><span data-stu-id="3a52e-124">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a52e-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a52e-125">-WorkspaceName</span></span>
<span data-ttu-id="3a52e-126">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a52e-126">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a52e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a52e-127">-DefaultProfile</span></span>
<span data-ttu-id="3a52e-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a52e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a52e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a52e-129">CommonParameters</span></span>
<span data-ttu-id="3a52e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a52e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a52e-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a52e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a52e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a52e-132">INPUTS</span></span>

## <span data-ttu-id="3a52e-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a52e-133">OUTPUTS</span></span>

## <span data-ttu-id="3a52e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a52e-134">NOTES</span></span>

## <span data-ttu-id="3a52e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a52e-135">RELATED LINKS</span></span>

[<span data-ttu-id="3a52e-136">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="3a52e-136">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


