---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: ad005dbf386bc8340fa0da0c5e8dac1d11bf4bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887765"
---
# <span data-ttu-id="b9551-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="b9551-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="b9551-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9551-102">SYNOPSIS</span></span>
<span data-ttu-id="b9551-103">Criar objeto PSHeaderAction.</span><span class="sxs-lookup"><span data-stu-id="b9551-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="b9551-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b9551-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9551-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b9551-105">DESCRIPTION</span></span>
<span data-ttu-id="b9551-106">Cria o objeto PSHeaderAction para a criação do objeto PSRulesEngineAction.</span><span class="sxs-lookup"><span data-stu-id="b9551-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="b9551-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9551-107">EXAMPLES</span></span>

### <span data-ttu-id="b9551-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9551-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="b9551-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b9551-109">PARAMETERS</span></span>

### <span data-ttu-id="b9551-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9551-110">-DefaultProfile</span></span>
<span data-ttu-id="b9551-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9551-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9551-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="b9551-112">-HeaderActionType</span></span>
<span data-ttu-id="b9551-113">Qual tipo de manipulação aplicar ao header.</span><span class="sxs-lookup"><span data-stu-id="b9551-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="b9551-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="b9551-114">-HeaderName</span></span>
<span data-ttu-id="b9551-115">O nome do header ao que essa ação se aplicará.</span><span class="sxs-lookup"><span data-stu-id="b9551-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="b9551-116">-Value</span><span class="sxs-lookup"><span data-stu-id="b9551-116">-Value</span></span>
<span data-ttu-id="b9551-117">O valor para atualizar o nome do header determinado com.</span><span class="sxs-lookup"><span data-stu-id="b9551-117">The value to update the given header name with.</span></span>
<span data-ttu-id="b9551-118">Esse valor não será usado se actionType for Delete.</span><span class="sxs-lookup"><span data-stu-id="b9551-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="b9551-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9551-119">CommonParameters</span></span>
<span data-ttu-id="b9551-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9551-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9551-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9551-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9551-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9551-122">INPUTS</span></span>

### <span data-ttu-id="b9551-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b9551-123">None</span></span>

## <span data-ttu-id="b9551-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b9551-124">OUTPUTS</span></span>

### <span data-ttu-id="b9551-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="b9551-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="b9551-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="b9551-126">NOTES</span></span>

## <span data-ttu-id="b9551-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9551-127">RELATED LINKS</span></span>
