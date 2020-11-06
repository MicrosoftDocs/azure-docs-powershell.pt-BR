---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: c636da952c02b4f2b4795cd1703c276a23a8221c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595702"
---
# <span data-ttu-id="efb7d-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="efb7d-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="efb7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efb7d-102">SYNOPSIS</span></span>
<span data-ttu-id="efb7d-103">Obtém uma lista ou uma descrição de serviço de gerenciamento de API específica.</span><span class="sxs-lookup"><span data-stu-id="efb7d-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="efb7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efb7d-104">SYNTAX</span></span>

### <span data-ttu-id="efb7d-105">GetBySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="efb7d-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efb7d-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="efb7d-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efb7d-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="efb7d-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="efb7d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="efb7d-108">DESCRIPTION</span></span>
<span data-ttu-id="efb7d-109">O cmdlet **Get-AzApiManagement** Obtém uma lista de todos os serviços de gerenciamento de API sob assinatura ou grupo de recursos especificado ou um gerenciamento de API específico.</span><span class="sxs-lookup"><span data-stu-id="efb7d-109">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="efb7d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="efb7d-110">EXAMPLES</span></span>

### <span data-ttu-id="efb7d-111">Exemplo 1: obter todos os serviços de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="efb7d-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="efb7d-112">Esse comando obtém todos os serviços de gerenciamento de API em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="efb7d-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="efb7d-113">Exemplo 2: obter todos os serviços de gerenciamento de API por um nome específico</span><span class="sxs-lookup"><span data-stu-id="efb7d-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="efb7d-114">Esse comando obtém todo o serviço de gerenciamento de API por nome.</span><span class="sxs-lookup"><span data-stu-id="efb7d-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="efb7d-115">OS</span><span class="sxs-lookup"><span data-stu-id="efb7d-115">PARAMETERS</span></span>

### <span data-ttu-id="efb7d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb7d-116">-DefaultProfile</span></span>
<span data-ttu-id="efb7d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="efb7d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efb7d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="efb7d-118">-Name</span></span>
<span data-ttu-id="efb7d-119">Especifica o nome do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="efb7d-119">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb7d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efb7d-120">-ResourceGroupName</span></span>
<span data-ttu-id="efb7d-121">Especifica o nome do grupo de recursos em que esse cmdlet obtém o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="efb7d-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb7d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb7d-122">CommonParameters</span></span>
<span data-ttu-id="efb7d-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efb7d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb7d-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efb7d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb7d-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="efb7d-125">INPUTS</span></span>

### <span data-ttu-id="efb7d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="efb7d-126">System.String</span></span>

## <span data-ttu-id="efb7d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="efb7d-127">OUTPUTS</span></span>

### <span data-ttu-id="efb7d-128">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="efb7d-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="efb7d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="efb7d-129">NOTES</span></span>

## <span data-ttu-id="efb7d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efb7d-130">RELATED LINKS</span></span>

[<span data-ttu-id="efb7d-131">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="efb7d-131">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="efb7d-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="efb7d-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="efb7d-133">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="efb7d-133">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="efb7d-134">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="efb7d-134">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


