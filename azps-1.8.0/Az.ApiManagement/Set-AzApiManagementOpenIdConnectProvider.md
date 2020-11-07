---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: fe320af601fad9d905471525b1a418c12c355f63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771333"
---
# <span data-ttu-id="a1b83-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a1b83-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="a1b83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1b83-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b83-103">Modifica um provedor OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="a1b83-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="a1b83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1b83-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1b83-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1b83-105">DESCRIPTION</span></span>
<span data-ttu-id="a1b83-106">O cmdlet **set-AzApiManagementOpenIdConnectProvider** modifica um provedor de conexão OpenID no gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b83-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="a1b83-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1b83-107">EXAMPLES</span></span>

### <span data-ttu-id="a1b83-108">Exemplo 1: alterar o segredo do cliente para um provedor</span><span class="sxs-lookup"><span data-stu-id="a1b83-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="a1b83-109">Esse comando modifica o provedor que tem a ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="a1b83-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="a1b83-110">O comando especifica um segredo do cliente para o provedor.</span><span class="sxs-lookup"><span data-stu-id="a1b83-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="a1b83-111">OS</span><span class="sxs-lookup"><span data-stu-id="a1b83-111">PARAMETERS</span></span>

### <span data-ttu-id="a1b83-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="a1b83-112">-ClientId</span></span>
<span data-ttu-id="a1b83-113">Especifica a ID do cliente do console de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="a1b83-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="a1b83-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="a1b83-114">-ClientSecret</span></span>
<span data-ttu-id="a1b83-115">Especifica o segredo do cliente do console de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="a1b83-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="a1b83-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a1b83-116">-Context</span></span>
<span data-ttu-id="a1b83-117">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a1b83-117">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b83-118">-DefaultProfile</span></span>
<span data-ttu-id="a1b83-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b83-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1b83-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a1b83-120">-Description</span></span>
<span data-ttu-id="a1b83-121">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="a1b83-121">Specifies a description.</span></span>

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

### <span data-ttu-id="a1b83-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="a1b83-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="a1b83-123">Especifica um URI de ponto de extremidade de metadados do provedor.</span><span class="sxs-lookup"><span data-stu-id="a1b83-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="a1b83-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1b83-124">-Name</span></span>
<span data-ttu-id="a1b83-125">Especifica um nome amigável para o provedor.</span><span class="sxs-lookup"><span data-stu-id="a1b83-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="a1b83-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="a1b83-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="a1b83-127">Especifica uma ID para o provedor que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a1b83-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="a1b83-128">Se você não especificar uma ID, esse cmdlet gerará uma.</span><span class="sxs-lookup"><span data-stu-id="a1b83-128">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b83-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1b83-129">-PassThru</span></span>
<span data-ttu-id="a1b83-130">Indica que esse cmdlet retorna o **PsApiManagementOpenIdConnectProvider** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a1b83-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b83-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b83-131">CommonParameters</span></span>
<span data-ttu-id="a1b83-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b83-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b83-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b83-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b83-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1b83-134">INPUTS</span></span>

### <span data-ttu-id="a1b83-135">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a1b83-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a1b83-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a1b83-136">System.String</span></span>

### <span data-ttu-id="a1b83-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a1b83-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a1b83-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1b83-138">OUTPUTS</span></span>

### <span data-ttu-id="a1b83-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a1b83-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="a1b83-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1b83-140">NOTES</span></span>

## <span data-ttu-id="a1b83-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1b83-141">RELATED LINKS</span></span>

[<span data-ttu-id="a1b83-142">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a1b83-142">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a1b83-143">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a1b83-143">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a1b83-144">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a1b83-144">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


