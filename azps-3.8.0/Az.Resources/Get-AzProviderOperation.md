---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 1ee29a4183dd78e9ced6d48e5f52c724e1b9a985
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942617"
---
# <span data-ttu-id="c609a-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="c609a-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="c609a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c609a-102">SYNOPSIS</span></span>
<span data-ttu-id="c609a-103">Obtém as operações de um provedor de recursos do Azure que é protegível usando o Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="c609a-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="c609a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c609a-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c609a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c609a-105">DESCRIPTION</span></span>
<span data-ttu-id="c609a-106">O Get-AzProviderOperation Obtém as operações expostas pelos provedores de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c609a-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="c609a-107">As operações podem ser compostas para criar funções personalizadas no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="c609a-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="c609a-108">O comando assume como entrada uma cadeia de caracteres de pesquisa de operação (com o caractere curinga (es) possível *) que determina os detalhes de operações a serem exibidos. Use Get-AzProviderOperation \* para obter todas as operações para todos os provedores de recursos do Azure. Use Get-AzProviderOperation Microsoft. Compute/* para obter todas as operações do provedor de recursos Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="c609a-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="c609a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c609a-109">EXAMPLES</span></span>

### <span data-ttu-id="c609a-110">Obter todas as ações para todos os provedores</span><span class="sxs-lookup"><span data-stu-id="c609a-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="c609a-111">Obter ações para um provedor de recursos específico</span><span class="sxs-lookup"><span data-stu-id="c609a-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="c609a-112">Obter todas as ações que podem ser executadas em máquinas virtuais</span><span class="sxs-lookup"><span data-stu-id="c609a-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="c609a-113">OS</span><span class="sxs-lookup"><span data-stu-id="c609a-113">PARAMETERS</span></span>

### <span data-ttu-id="c609a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c609a-114">-DefaultProfile</span></span>
<span data-ttu-id="c609a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c609a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c609a-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="c609a-116">-OperationSearchString</span></span>
<span data-ttu-id="c609a-117">A cadeia de caracteres de pesquisa da operação (com caracteres curinga possíveis (\*))</span><span class="sxs-lookup"><span data-stu-id="c609a-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="c609a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c609a-118">CommonParameters</span></span>
<span data-ttu-id="c609a-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c609a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c609a-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c609a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c609a-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c609a-121">INPUTS</span></span>

### <span data-ttu-id="c609a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c609a-122">System.String</span></span>

## <span data-ttu-id="c609a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c609a-123">OUTPUTS</span></span>

### <span data-ttu-id="c609a-124">Microsoft. Azure. Commands. Resources. Models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="c609a-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="c609a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c609a-125">NOTES</span></span>
<span data-ttu-id="c609a-126">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="c609a-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c609a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c609a-127">RELATED LINKS</span></span>
