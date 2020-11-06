---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/get-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
ms.openlocfilehash: d0140af9d5345e9f3f68c212ae43403fc0f64280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429563"
---
# <span data-ttu-id="77d74-101">Get-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="77d74-101">Get-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="77d74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77d74-102">SYNOPSIS</span></span>
<span data-ttu-id="77d74-103">Obtenha ou liste o controlador DevSpaces do Azure.</span><span class="sxs-lookup"><span data-stu-id="77d74-103">Get or list Azure DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77d74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77d74-104">SYNTAX</span></span>

### <span data-ttu-id="77d74-105">ListDevSpacesControllerParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="77d74-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzureRmDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77d74-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="77d74-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77d74-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77d74-107">DESCRIPTION</span></span>
<span data-ttu-id="77d74-108">Obtenha ou liste o controlador DevSpaces do Azure.</span><span class="sxs-lookup"><span data-stu-id="77d74-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="77d74-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77d74-109">EXAMPLES</span></span>

### <span data-ttu-id="77d74-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="77d74-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="77d74-111">Listar todos os controladores em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="77d74-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="77d74-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="77d74-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="77d74-113">Obter um controlador DevSpaces em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="77d74-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="77d74-114">OS</span><span class="sxs-lookup"><span data-stu-id="77d74-114">PARAMETERS</span></span>

### <span data-ttu-id="77d74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d74-115">-DefaultProfile</span></span>
<span data-ttu-id="77d74-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77d74-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77d74-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="77d74-117">-Name</span></span>
<span data-ttu-id="77d74-118">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="77d74-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="77d74-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77d74-119">-ResourceGroupName</span></span>
<span data-ttu-id="77d74-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="77d74-120">Resource group name</span></span>

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

### <span data-ttu-id="77d74-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d74-121">CommonParameters</span></span>
<span data-ttu-id="77d74-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77d74-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d74-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77d74-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d74-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77d74-124">INPUTS</span></span>

### <span data-ttu-id="77d74-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="77d74-125">None</span></span>

## <span data-ttu-id="77d74-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77d74-126">OUTPUTS</span></span>

### <span data-ttu-id="77d74-127">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="77d74-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="77d74-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77d74-128">NOTES</span></span>

## <span data-ttu-id="77d74-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77d74-129">RELATED LINKS</span></span>
