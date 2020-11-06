---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 7cc4c61073b0b196faca8d95bd5153abe2587ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596625"
---
# <span data-ttu-id="75eb9-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="75eb9-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="75eb9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="75eb9-103">Obtenha ou liste o controlador DevSpaces do Azure.</span><span class="sxs-lookup"><span data-stu-id="75eb9-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="75eb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75eb9-104">SYNTAX</span></span>

### <span data-ttu-id="75eb9-105">ListDevSpacesControllerParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="75eb9-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75eb9-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75eb9-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75eb9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75eb9-107">DESCRIPTION</span></span>
<span data-ttu-id="75eb9-108">Obtenha ou liste o controlador DevSpaces do Azure.</span><span class="sxs-lookup"><span data-stu-id="75eb9-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="75eb9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75eb9-109">EXAMPLES</span></span>

### <span data-ttu-id="75eb9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75eb9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="75eb9-111">Listar todos os controladores em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="75eb9-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="75eb9-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="75eb9-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="75eb9-113">Obter um controlador DevSpaces em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="75eb9-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="75eb9-114">OS</span><span class="sxs-lookup"><span data-stu-id="75eb9-114">PARAMETERS</span></span>

### <span data-ttu-id="75eb9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75eb9-115">-DefaultProfile</span></span>
<span data-ttu-id="75eb9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75eb9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75eb9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="75eb9-117">-Name</span></span>
<span data-ttu-id="75eb9-118">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="75eb9-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="75eb9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75eb9-119">-ResourceGroupName</span></span>
<span data-ttu-id="75eb9-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="75eb9-120">Resource group name</span></span>

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

### <span data-ttu-id="75eb9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75eb9-121">CommonParameters</span></span>
<span data-ttu-id="75eb9-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75eb9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75eb9-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75eb9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75eb9-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75eb9-124">INPUTS</span></span>

### <span data-ttu-id="75eb9-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="75eb9-125">None</span></span>

## <span data-ttu-id="75eb9-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75eb9-126">OUTPUTS</span></span>

### <span data-ttu-id="75eb9-127">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="75eb9-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="75eb9-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75eb9-128">NOTES</span></span>

## <span data-ttu-id="75eb9-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75eb9-129">RELATED LINKS</span></span>
