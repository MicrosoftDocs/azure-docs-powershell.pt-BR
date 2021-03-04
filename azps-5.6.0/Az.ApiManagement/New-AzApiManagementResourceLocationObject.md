---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 88b2ae64430f73df242d7003baa2c72ec6512dce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886698"
---
# <span data-ttu-id="5c9af-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="5c9af-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="5c9af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c9af-102">SYNOPSIS</span></span>
<span data-ttu-id="5c9af-103">Crie um novo contrato de local de recurso (usado em Gateways).</span><span class="sxs-lookup"><span data-stu-id="5c9af-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="5c9af-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5c9af-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c9af-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5c9af-105">DESCRIPTION</span></span>
<span data-ttu-id="5c9af-106">O cmdlet **New-AzApiManagementResourceLocationObject** cria um novo contrato de local de recurso (usado em Gateways).</span><span class="sxs-lookup"><span data-stu-id="5c9af-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="5c9af-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c9af-107">EXAMPLES</span></span>

### <span data-ttu-id="5c9af-108">Exemplo 1: Criar um contrato de localização de recurso</span><span class="sxs-lookup"><span data-stu-id="5c9af-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="5c9af-109">Este comando cria um local de recurso.</span><span class="sxs-lookup"><span data-stu-id="5c9af-109">This command creates a resource location.</span></span>

## <span data-ttu-id="5c9af-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5c9af-110">PARAMETERS</span></span>

### <span data-ttu-id="5c9af-111">-City</span><span class="sxs-lookup"><span data-stu-id="5c9af-111">-City</span></span>
<span data-ttu-id="5c9af-112">Cidade do Local.</span><span class="sxs-lookup"><span data-stu-id="5c9af-112">Location City.</span></span>
<span data-ttu-id="5c9af-113">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5c9af-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="5c9af-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="5c9af-114">-CountryOrRegion</span></span>
<span data-ttu-id="5c9af-115">Local País ou Região.</span><span class="sxs-lookup"><span data-stu-id="5c9af-115">Location Country or Region.</span></span>
<span data-ttu-id="5c9af-116">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5c9af-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="5c9af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c9af-117">-DefaultProfile</span></span>
<span data-ttu-id="5c9af-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c9af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c9af-119">-District</span><span class="sxs-lookup"><span data-stu-id="5c9af-119">-District</span></span>
<span data-ttu-id="5c9af-120">Location District.</span><span class="sxs-lookup"><span data-stu-id="5c9af-120">Location District.</span></span>
<span data-ttu-id="5c9af-121">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5c9af-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="5c9af-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5c9af-122">-Name</span></span>
<span data-ttu-id="5c9af-123">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="5c9af-123">Location Name.</span></span>
<span data-ttu-id="5c9af-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="5c9af-124">This parameter is required.</span></span>

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

### <span data-ttu-id="5c9af-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c9af-125">CommonParameters</span></span>
<span data-ttu-id="5c9af-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c9af-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c9af-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c9af-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c9af-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c9af-128">INPUTS</span></span>

### <span data-ttu-id="5c9af-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5c9af-129">None</span></span>

## <span data-ttu-id="5c9af-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5c9af-130">OUTPUTS</span></span>

### <span data-ttu-id="5c9af-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="5c9af-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="5c9af-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="5c9af-132">NOTES</span></span>

## <span data-ttu-id="5c9af-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c9af-133">RELATED LINKS</span></span>
