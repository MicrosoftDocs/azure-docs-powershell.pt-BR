---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113336"
---
# <span data-ttu-id="47ae3-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="47ae3-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="47ae3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="47ae3-103">Obtém as operações de um provedor de recursos do Azure que são recuráveis usando o Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="47ae3-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="47ae3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47ae3-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47ae3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="47ae3-105">DESCRIPTION</span></span>
<span data-ttu-id="47ae3-106">A Get-AzProviderOperation obtém as operações expostas pelos provedores de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="47ae3-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="47ae3-107">As operações podem ser compostas para criar funções personalizadas no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="47ae3-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="47ae3-108">O comando assume como entrada uma cadeia de caracteres de pesquisa de operação (com possíveis caracteres curinga( ) que determina os detalhes *das operações a exibir. Use Get-AzProviderOperation \* para obter todas as operações para todos os provedores de recursos do Azure. Use Get-AzProviderOperation Microsoft.Compute/ para* obter todas as operações do provedor de recursos Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="47ae3-108">The command takes as input an operation search string (with possible wildcard(*) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="47ae3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47ae3-109">EXAMPLES</span></span>

### <span data-ttu-id="47ae3-110">Exemplo 1: Obter todas as ações para todos os provedores</span><span class="sxs-lookup"><span data-stu-id="47ae3-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="47ae3-111">Exemplo 2: Obter ações para um provedor de recursos específico</span><span class="sxs-lookup"><span data-stu-id="47ae3-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="47ae3-112">Exemplo 3: Obter todas as ações que podem ser executadas em máquinas virtuais</span><span class="sxs-lookup"><span data-stu-id="47ae3-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="47ae3-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47ae3-113">PARAMETERS</span></span>

### <span data-ttu-id="47ae3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ae3-114">-DefaultProfile</span></span>
<span data-ttu-id="47ae3-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="47ae3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47ae3-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="47ae3-116">-OperationSearchString</span></span>
<span data-ttu-id="47ae3-117">A cadeia de caracteres de pesquisa de operação (com possíveis caracteres curinga (\*)</span><span class="sxs-lookup"><span data-stu-id="47ae3-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="47ae3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ae3-118">CommonParameters</span></span>
<span data-ttu-id="47ae3-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ae3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ae3-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47ae3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ae3-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="47ae3-121">INPUTS</span></span>

### <span data-ttu-id="47ae3-122">System.String</span><span class="sxs-lookup"><span data-stu-id="47ae3-122">System.String</span></span>

## <span data-ttu-id="47ae3-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="47ae3-123">OUTPUTS</span></span>

### <span data-ttu-id="47ae3-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="47ae3-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="47ae3-125">Notas</span><span class="sxs-lookup"><span data-stu-id="47ae3-125">NOTES</span></span>
<span data-ttu-id="47ae3-126">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="47ae3-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="47ae3-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47ae3-127">RELATED LINKS</span></span>
