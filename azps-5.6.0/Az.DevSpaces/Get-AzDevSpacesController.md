---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: dd7ba99632cfef493fe3202b2402a938b11fa807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886481"
---
# <span data-ttu-id="134d3-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="134d3-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="134d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="134d3-102">SYNOPSIS</span></span>
<span data-ttu-id="134d3-103">Obter ou listar o controlador do Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="134d3-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="134d3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="134d3-104">SYNTAX</span></span>

### <span data-ttu-id="134d3-105">ListDevSpacesControllerParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="134d3-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="134d3-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="134d3-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="134d3-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="134d3-107">DESCRIPTION</span></span>
<span data-ttu-id="134d3-108">Obter ou listar o controlador do Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="134d3-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="134d3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="134d3-109">EXAMPLES</span></span>

### <span data-ttu-id="134d3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="134d3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="134d3-111">Listar todos os controladores em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="134d3-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="134d3-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="134d3-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="134d3-113">Obter controladores DevSpaces em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="134d3-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="134d3-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="134d3-114">PARAMETERS</span></span>

### <span data-ttu-id="134d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="134d3-115">-DefaultProfile</span></span>
<span data-ttu-id="134d3-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="134d3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="134d3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="134d3-117">-Name</span></span>
<span data-ttu-id="134d3-118">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="134d3-118">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="134d3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="134d3-119">-ResourceGroupName</span></span>
<span data-ttu-id="134d3-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="134d3-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ListDevSpacesControllerParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="134d3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="134d3-121">CommonParameters</span></span>
<span data-ttu-id="134d3-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="134d3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="134d3-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="134d3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="134d3-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="134d3-124">INPUTS</span></span>

### <span data-ttu-id="134d3-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="134d3-125">None</span></span>

## <span data-ttu-id="134d3-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="134d3-126">OUTPUTS</span></span>

### <span data-ttu-id="134d3-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="134d3-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="134d3-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="134d3-128">NOTES</span></span>

## <span data-ttu-id="134d3-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="134d3-129">RELATED LINKS</span></span>
