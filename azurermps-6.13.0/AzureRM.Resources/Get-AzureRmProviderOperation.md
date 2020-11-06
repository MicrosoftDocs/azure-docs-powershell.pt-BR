---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: ff56fc9df0d2303938700d85323a98575d1fb0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429381"
---
# <span data-ttu-id="48168-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="48168-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="48168-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48168-102">SYNOPSIS</span></span>
<span data-ttu-id="48168-103">Obtém as operações de um provedor de recursos do Azure que é protegível usando o Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="48168-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48168-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48168-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48168-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48168-105">DESCRIPTION</span></span>
<span data-ttu-id="48168-106">O Get-AzureRmProviderOperation Obtém as operações expostas pelos provedores de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="48168-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="48168-107">As operações podem ser compostas para criar funções personalizadas no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="48168-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="48168-108">O comando assume como entrada uma cadeia de caracteres de pesquisa de operação (com o caractere curinga (es) possível *) que determina os detalhes de operações a serem exibidos. Use Get-AzureRmProviderOperation \* para obter todas as operações para todos os provedores de recursos do Azure. Use Get-AzureRmProviderOperation Microsoft. Compute/* para obter todas as operações do provedor de recursos Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="48168-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzureRmProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="48168-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48168-109">EXAMPLES</span></span>

### <span data-ttu-id="48168-110">Obter todas as ações para todos os provedores</span><span class="sxs-lookup"><span data-stu-id="48168-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="48168-111">Obter ações para um provedor de recursos específico</span><span class="sxs-lookup"><span data-stu-id="48168-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="48168-112">Obter todas as ações que podem ser executadas em máquinas virtuais</span><span class="sxs-lookup"><span data-stu-id="48168-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="48168-113">OS</span><span class="sxs-lookup"><span data-stu-id="48168-113">PARAMETERS</span></span>

### <span data-ttu-id="48168-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48168-114">-DefaultProfile</span></span>
<span data-ttu-id="48168-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="48168-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48168-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="48168-116">-OperationSearchString</span></span>
<span data-ttu-id="48168-117">A cadeia de caracteres de pesquisa da operação (com caracteres curinga possíveis (\*))</span><span class="sxs-lookup"><span data-stu-id="48168-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48168-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48168-118">CommonParameters</span></span>
<span data-ttu-id="48168-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48168-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48168-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48168-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48168-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48168-121">INPUTS</span></span>

### <span data-ttu-id="48168-122">System. String</span><span class="sxs-lookup"><span data-stu-id="48168-122">System.String</span></span>
<span data-ttu-id="48168-123">Parâmetros: OperationSearchString (ByValue)</span><span class="sxs-lookup"><span data-stu-id="48168-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="48168-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48168-124">OUTPUTS</span></span>

### <span data-ttu-id="48168-125">Microsoft. Azure. Commands. Resources. Models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="48168-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="48168-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48168-126">NOTES</span></span>
<span data-ttu-id="48168-127">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="48168-127">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="48168-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48168-128">RELATED LINKS</span></span>
