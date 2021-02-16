---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117653"
---
# <span data-ttu-id="c817c-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="c817c-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="c817c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c817c-102">SYNOPSIS</span></span>
<span data-ttu-id="c817c-103">Criar objeto PSHeaderAction.</span><span class="sxs-lookup"><span data-stu-id="c817c-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="c817c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c817c-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c817c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c817c-105">DESCRIPTION</span></span>
<span data-ttu-id="c817c-106">Cria um objeto PSHeaderAction para a criação do objeto PSRulesEngineAction.</span><span class="sxs-lookup"><span data-stu-id="c817c-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="c817c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c817c-107">EXAMPLES</span></span>

### <span data-ttu-id="c817c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c817c-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="c817c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c817c-109">PARAMETERS</span></span>

### <span data-ttu-id="c817c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c817c-110">-DefaultProfile</span></span>
<span data-ttu-id="c817c-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c817c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c817c-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="c817c-112">-HeaderActionType</span></span>
<span data-ttu-id="c817c-113">Que tipo de manipulação aplicar ao header.</span><span class="sxs-lookup"><span data-stu-id="c817c-113">Which type of manipulation to apply to the header.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderActionType
Parameter Sets: (All)
Aliases:
Accepted values: Append, Delete, Overwrite

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c817c-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="c817c-114">-HeaderName</span></span>
<span data-ttu-id="c817c-115">O nome do header ao que esta ação se aplicará.</span><span class="sxs-lookup"><span data-stu-id="c817c-115">The name of the header this action will apply to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c817c-116">-Valor</span><span class="sxs-lookup"><span data-stu-id="c817c-116">-Value</span></span>
<span data-ttu-id="c817c-117">O valor com o que atualizar o nome do determinado header.</span><span class="sxs-lookup"><span data-stu-id="c817c-117">The value to update the given header name with.</span></span>
<span data-ttu-id="c817c-118">Esse valor não será usado se o actionType for Delete.</span><span class="sxs-lookup"><span data-stu-id="c817c-118">This value is not used if the actionType is Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c817c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c817c-119">CommonParameters</span></span>
<span data-ttu-id="c817c-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c817c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c817c-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c817c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c817c-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="c817c-122">INPUTS</span></span>

### <span data-ttu-id="c817c-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c817c-123">None</span></span>

## <span data-ttu-id="c817c-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="c817c-124">OUTPUTS</span></span>

### <span data-ttu-id="c817c-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderaction</span><span class="sxs-lookup"><span data-stu-id="c817c-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="c817c-126">Notas</span><span class="sxs-lookup"><span data-stu-id="c817c-126">NOTES</span></span>

## <span data-ttu-id="c817c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c817c-127">RELATED LINKS</span></span>
