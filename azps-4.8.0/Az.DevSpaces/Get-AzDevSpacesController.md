---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 56b26c48316fbcf5c0000a6904c71a655962aae0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955597"
---
# <span data-ttu-id="6d871-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="6d871-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="6d871-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d871-102">SYNOPSIS</span></span>
<span data-ttu-id="6d871-103">Obtenha ou liste o controlador DevSpaces do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d871-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="6d871-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d871-104">SYNTAX</span></span>

### <span data-ttu-id="6d871-105">ListDevSpacesControllerParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6d871-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d871-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d871-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d871-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d871-107">DESCRIPTION</span></span>
<span data-ttu-id="6d871-108">Obtenha ou liste o controlador DevSpaces do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d871-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="6d871-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d871-109">EXAMPLES</span></span>

### <span data-ttu-id="6d871-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d871-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="6d871-111">Listar todos os controladores em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="6d871-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="6d871-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6d871-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="6d871-113">Obter um controlador DevSpaces em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="6d871-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="6d871-114">OS</span><span class="sxs-lookup"><span data-stu-id="6d871-114">PARAMETERS</span></span>

### <span data-ttu-id="6d871-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d871-115">-DefaultProfile</span></span>
<span data-ttu-id="6d871-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d871-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d871-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d871-117">-Name</span></span>
<span data-ttu-id="6d871-118">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="6d871-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="6d871-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d871-119">-ResourceGroupName</span></span>
<span data-ttu-id="6d871-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6d871-120">Resource group name</span></span>

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

### <span data-ttu-id="6d871-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d871-121">CommonParameters</span></span>
<span data-ttu-id="6d871-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d871-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d871-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d871-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d871-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d871-124">INPUTS</span></span>

### <span data-ttu-id="6d871-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6d871-125">None</span></span>

## <span data-ttu-id="6d871-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d871-126">OUTPUTS</span></span>

### <span data-ttu-id="6d871-127">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="6d871-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="6d871-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d871-128">NOTES</span></span>

## <span data-ttu-id="6d871-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d871-129">RELATED LINKS</span></span>
