---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432651"
---
# <span data-ttu-id="1cbc8-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1cbc8-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="1cbc8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cbc8-102">SYNOPSIS</span></span>
<span data-ttu-id="1cbc8-103">Cria uma nova entidade de gateway.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="1cbc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cbc8-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cbc8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cbc8-105">DESCRIPTION</span></span>
<span data-ttu-id="1cbc8-106">O cmdlet **New-AzApiManagementGateway** cria uma nova entidade de gateway.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="1cbc8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cbc8-107">EXAMPLES</span></span>

### <span data-ttu-id="1cbc8-108">Exemplo 1: criar um gateway</span><span class="sxs-lookup"><span data-stu-id="1cbc8-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="1cbc8-109">Esse comando cria um gateway.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-109">This command creates a gateway.</span></span>

## <span data-ttu-id="1cbc8-110">OS</span><span class="sxs-lookup"><span data-stu-id="1cbc8-110">PARAMETERS</span></span>

### <span data-ttu-id="1cbc8-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1cbc8-111">-Context</span></span>
<span data-ttu-id="1cbc8-112">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1cbc8-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbc8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cbc8-114">-DefaultProfile</span></span>
<span data-ttu-id="1cbc8-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cbc8-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="1cbc8-116">-Description</span></span>
<span data-ttu-id="1cbc8-117">Descrição do gateway.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-117">Gateway description.</span></span>
<span data-ttu-id="1cbc8-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbc8-119">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="1cbc8-119">-GatewayId</span></span>
<span data-ttu-id="1cbc8-120">Identificador do novo gateway.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-120">Identifier of new gateway.</span></span>
<span data-ttu-id="1cbc8-121">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-121">This parameter is optional.</span></span>
<span data-ttu-id="1cbc8-122">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-122">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbc8-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="1cbc8-123">-LocationData</span></span>
<span data-ttu-id="1cbc8-124">Localização do gateway.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-124">Gateway location.</span></span>
<span data-ttu-id="1cbc8-125">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbc8-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1cbc8-126">-Confirm</span></span>
<span data-ttu-id="1cbc8-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbc8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cbc8-128">-WhatIf</span></span>
<span data-ttu-id="1cbc8-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1cbc8-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbc8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cbc8-131">CommonParameters</span></span>
<span data-ttu-id="1cbc8-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cbc8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cbc8-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cbc8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cbc8-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cbc8-134">INPUTS</span></span>

### <span data-ttu-id="1cbc8-135">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1cbc8-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1cbc8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1cbc8-136">System.String</span></span>

### <span data-ttu-id="1cbc8-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="1cbc8-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="1cbc8-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cbc8-138">OUTPUTS</span></span>

### <span data-ttu-id="1cbc8-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1cbc8-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="1cbc8-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cbc8-140">NOTES</span></span>

## <span data-ttu-id="1cbc8-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cbc8-141">RELATED LINKS</span></span>
