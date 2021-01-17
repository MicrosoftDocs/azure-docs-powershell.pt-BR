---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429358"
---
# <span data-ttu-id="0412d-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="0412d-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="0412d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0412d-102">SYNOPSIS</span></span>
<span data-ttu-id="0412d-103">Criar objeto PSHeaderAction.</span><span class="sxs-lookup"><span data-stu-id="0412d-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="0412d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0412d-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0412d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0412d-105">DESCRIPTION</span></span>
<span data-ttu-id="0412d-106">Cria o objeto PSHeaderAction para a criação do objeto PSRulesEngineAction.</span><span class="sxs-lookup"><span data-stu-id="0412d-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="0412d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0412d-107">EXAMPLES</span></span>

### <span data-ttu-id="0412d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0412d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="0412d-109">OS</span><span class="sxs-lookup"><span data-stu-id="0412d-109">PARAMETERS</span></span>

### <span data-ttu-id="0412d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0412d-110">-DefaultProfile</span></span>
<span data-ttu-id="0412d-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0412d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0412d-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="0412d-112">-HeaderActionType</span></span>
<span data-ttu-id="0412d-113">O tipo de manipulação a ser aplicado ao cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="0412d-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="0412d-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="0412d-114">-HeaderName</span></span>
<span data-ttu-id="0412d-115">O nome do cabeçalho ao qual esta ação será aplicada.</span><span class="sxs-lookup"><span data-stu-id="0412d-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="0412d-116">-Valor</span><span class="sxs-lookup"><span data-stu-id="0412d-116">-Value</span></span>
<span data-ttu-id="0412d-117">O valor com o qual atualizar o nome do cabeçalho fornecido.</span><span class="sxs-lookup"><span data-stu-id="0412d-117">The value to update the given header name with.</span></span>
<span data-ttu-id="0412d-118">Esse valor não será usado se o ActionType for DELETE.</span><span class="sxs-lookup"><span data-stu-id="0412d-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="0412d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0412d-119">CommonParameters</span></span>
<span data-ttu-id="0412d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0412d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0412d-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0412d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0412d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0412d-122">INPUTS</span></span>

### <span data-ttu-id="0412d-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0412d-123">None</span></span>

## <span data-ttu-id="0412d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0412d-124">OUTPUTS</span></span>

### <span data-ttu-id="0412d-125">Microsoft. Azure. Commands. FrontDoor. Models. PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="0412d-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="0412d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0412d-126">NOTES</span></span>

## <span data-ttu-id="0412d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0412d-127">RELATED LINKS</span></span>
