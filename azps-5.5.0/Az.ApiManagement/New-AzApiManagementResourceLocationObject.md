---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118048"
---
# <span data-ttu-id="07ea3-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="07ea3-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="07ea3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="07ea3-103">Criar um novo contrato de localização de recursos (usado em Gateways).</span><span class="sxs-lookup"><span data-stu-id="07ea3-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="07ea3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07ea3-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07ea3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="07ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="07ea3-106">O cmdlet **New-AzApiManagementResourceLocationObject** cria um novo contrato de localização de recursos (usado em Gateways).</span><span class="sxs-lookup"><span data-stu-id="07ea3-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="07ea3-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="07ea3-107">EXAMPLES</span></span>

### <span data-ttu-id="07ea3-108">Exemplo 1: Criar um contrato de localização de recursos</span><span class="sxs-lookup"><span data-stu-id="07ea3-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="07ea3-109">Esse comando cria um local de recurso.</span><span class="sxs-lookup"><span data-stu-id="07ea3-109">This command creates a resource location.</span></span>

## <span data-ttu-id="07ea3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07ea3-110">PARAMETERS</span></span>

### <span data-ttu-id="07ea3-111">-Cidade</span><span class="sxs-lookup"><span data-stu-id="07ea3-111">-City</span></span>
<span data-ttu-id="07ea3-112">Cidade do Local.</span><span class="sxs-lookup"><span data-stu-id="07ea3-112">Location City.</span></span>
<span data-ttu-id="07ea3-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="07ea3-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="07ea3-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="07ea3-114">-CountryOrRegion</span></span>
<span data-ttu-id="07ea3-115">País ou Região de Localização.</span><span class="sxs-lookup"><span data-stu-id="07ea3-115">Location Country or Region.</span></span>
<span data-ttu-id="07ea3-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="07ea3-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="07ea3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ea3-117">-DefaultProfile</span></span>
<span data-ttu-id="07ea3-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07ea3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07ea3-119">-Distrito</span><span class="sxs-lookup"><span data-stu-id="07ea3-119">-District</span></span>
<span data-ttu-id="07ea3-120">Distrito de Localização.</span><span class="sxs-lookup"><span data-stu-id="07ea3-120">Location District.</span></span>
<span data-ttu-id="07ea3-121">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="07ea3-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="07ea3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="07ea3-122">-Name</span></span>
<span data-ttu-id="07ea3-123">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="07ea3-123">Location Name.</span></span>
<span data-ttu-id="07ea3-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="07ea3-124">This parameter is required.</span></span>

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

### <span data-ttu-id="07ea3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ea3-125">CommonParameters</span></span>
<span data-ttu-id="07ea3-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ea3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ea3-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07ea3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ea3-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="07ea3-128">INPUTS</span></span>

### <span data-ttu-id="07ea3-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="07ea3-129">None</span></span>

## <span data-ttu-id="07ea3-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="07ea3-130">OUTPUTS</span></span>

### <span data-ttu-id="07ea3-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="07ea3-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="07ea3-132">Notas</span><span class="sxs-lookup"><span data-stu-id="07ea3-132">NOTES</span></span>

## <span data-ttu-id="07ea3-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07ea3-133">RELATED LINKS</span></span>
