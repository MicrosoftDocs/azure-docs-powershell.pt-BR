---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117094"
---
# <span data-ttu-id="be570-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="be570-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="be570-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be570-102">SYNOPSIS</span></span>
<span data-ttu-id="be570-103">Criar um novo contrato de localização de recursos (usado em gateways).</span><span class="sxs-lookup"><span data-stu-id="be570-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="be570-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be570-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be570-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be570-105">DESCRIPTION</span></span>
<span data-ttu-id="be570-106">O cmdlet **New-AzApiManagementResourceLocationObject** cria um novo contrato de localização de recursos (usado em gateways).</span><span class="sxs-lookup"><span data-stu-id="be570-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="be570-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be570-107">EXAMPLES</span></span>

### <span data-ttu-id="be570-108">Exemplo 1: criar um contrato de localização de recursos</span><span class="sxs-lookup"><span data-stu-id="be570-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="be570-109">Esse comando cria um local do recurso.</span><span class="sxs-lookup"><span data-stu-id="be570-109">This command creates a resource location.</span></span>

## <span data-ttu-id="be570-110">OS</span><span class="sxs-lookup"><span data-stu-id="be570-110">PARAMETERS</span></span>

### <span data-ttu-id="be570-111">-Cidade</span><span class="sxs-lookup"><span data-stu-id="be570-111">-City</span></span>
<span data-ttu-id="be570-112">Cidade do local.</span><span class="sxs-lookup"><span data-stu-id="be570-112">Location City.</span></span>
<span data-ttu-id="be570-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="be570-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="be570-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="be570-114">-CountryOrRegion</span></span>
<span data-ttu-id="be570-115">País ou região do local.</span><span class="sxs-lookup"><span data-stu-id="be570-115">Location Country or Region.</span></span>
<span data-ttu-id="be570-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="be570-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="be570-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be570-117">-DefaultProfile</span></span>
<span data-ttu-id="be570-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be570-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be570-119">-Distrito</span><span class="sxs-lookup"><span data-stu-id="be570-119">-District</span></span>
<span data-ttu-id="be570-120">Distrito de localização.</span><span class="sxs-lookup"><span data-stu-id="be570-120">Location District.</span></span>
<span data-ttu-id="be570-121">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="be570-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="be570-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="be570-122">-Name</span></span>
<span data-ttu-id="be570-123">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="be570-123">Location Name.</span></span>
<span data-ttu-id="be570-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="be570-124">This parameter is required.</span></span>

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

### <span data-ttu-id="be570-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be570-125">CommonParameters</span></span>
<span data-ttu-id="be570-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be570-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be570-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be570-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be570-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be570-128">INPUTS</span></span>

### <span data-ttu-id="be570-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="be570-129">None</span></span>

## <span data-ttu-id="be570-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be570-130">OUTPUTS</span></span>

### <span data-ttu-id="be570-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="be570-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="be570-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be570-132">NOTES</span></span>

## <span data-ttu-id="be570-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be570-133">RELATED LINKS</span></span>
