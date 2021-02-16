---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 56b26c48316fbcf5c0000a6904c71a655962aae0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117690"
---
# <span data-ttu-id="28046-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="28046-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="28046-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28046-102">SYNOPSIS</span></span>
<span data-ttu-id="28046-103">Obter ou listar o controlador do Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="28046-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="28046-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28046-104">SYNTAX</span></span>

### <span data-ttu-id="28046-105">ListDevSpacesControllerParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="28046-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28046-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="28046-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28046-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="28046-107">DESCRIPTION</span></span>
<span data-ttu-id="28046-108">Obter ou listar o controlador do Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="28046-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="28046-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="28046-109">EXAMPLES</span></span>

### <span data-ttu-id="28046-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28046-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="28046-111">Listar todos os controladores de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="28046-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="28046-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="28046-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="28046-113">Obter controladores de DevSpaces em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="28046-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="28046-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28046-114">PARAMETERS</span></span>

### <span data-ttu-id="28046-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28046-115">-DefaultProfile</span></span>
<span data-ttu-id="28046-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28046-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28046-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="28046-117">-Name</span></span>
<span data-ttu-id="28046-118">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="28046-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="28046-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28046-119">-ResourceGroupName</span></span>
<span data-ttu-id="28046-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="28046-120">Resource group name</span></span>

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

### <span data-ttu-id="28046-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28046-121">CommonParameters</span></span>
<span data-ttu-id="28046-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28046-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28046-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28046-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28046-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="28046-124">INPUTS</span></span>

### <span data-ttu-id="28046-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="28046-125">None</span></span>

## <span data-ttu-id="28046-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="28046-126">OUTPUTS</span></span>

### <span data-ttu-id="28046-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="28046-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="28046-128">Notas</span><span class="sxs-lookup"><span data-stu-id="28046-128">NOTES</span></span>

## <span data-ttu-id="28046-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28046-129">RELATED LINKS</span></span>
