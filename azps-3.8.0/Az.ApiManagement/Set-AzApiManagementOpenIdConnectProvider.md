---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 4bceb472fb3971b177f53b43fc48ad00c1422b58
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944181"
---
# <span data-ttu-id="7aa73-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="7aa73-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="7aa73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7aa73-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa73-103">Modifica um provedor OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="7aa73-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="7aa73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7aa73-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7aa73-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7aa73-105">DESCRIPTION</span></span>
<span data-ttu-id="7aa73-106">O cmdlet **set-AzApiManagementOpenIdConnectProvider** modifica um provedor de conexão OpenID no gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="7aa73-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="7aa73-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7aa73-107">EXAMPLES</span></span>

### <span data-ttu-id="7aa73-108">Exemplo 1: alterar o segredo do cliente para um provedor</span><span class="sxs-lookup"><span data-stu-id="7aa73-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="7aa73-109">Esse comando modifica o provedor que tem a ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="7aa73-109">This command modifies the provider that has the ID OICProvider01.</span></span>
<span data-ttu-id="7aa73-110">O comando especifica um segredo do cliente para o provedor.</span><span class="sxs-lookup"><span data-stu-id="7aa73-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="7aa73-111">OS</span><span class="sxs-lookup"><span data-stu-id="7aa73-111">PARAMETERS</span></span>

### <span data-ttu-id="7aa73-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="7aa73-112">-ClientId</span></span>
<span data-ttu-id="7aa73-113">Especifica a ID do cliente do console de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="7aa73-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="7aa73-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="7aa73-114">-ClientSecret</span></span>
<span data-ttu-id="7aa73-115">Especifica o segredo do cliente do console de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="7aa73-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="7aa73-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7aa73-116">-Context</span></span>
<span data-ttu-id="7aa73-117">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7aa73-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7aa73-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa73-118">-DefaultProfile</span></span>
<span data-ttu-id="7aa73-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7aa73-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aa73-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="7aa73-120">-Description</span></span>
<span data-ttu-id="7aa73-121">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="7aa73-121">Specifies a description.</span></span>

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

### <span data-ttu-id="7aa73-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="7aa73-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="7aa73-123">Especifica um URI de ponto de extremidade de metadados do provedor.</span><span class="sxs-lookup"><span data-stu-id="7aa73-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="7aa73-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7aa73-124">-Name</span></span>
<span data-ttu-id="7aa73-125">Especifica um nome amigável para o provedor.</span><span class="sxs-lookup"><span data-stu-id="7aa73-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="7aa73-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="7aa73-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="7aa73-127">Especifica uma ID para o provedor que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="7aa73-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="7aa73-128">Se você não especificar uma ID, esse cmdlet gerará uma.</span><span class="sxs-lookup"><span data-stu-id="7aa73-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="7aa73-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7aa73-129">-PassThru</span></span>
<span data-ttu-id="7aa73-130">Indica que esse cmdlet retorna o **PsApiManagementOpenIdConnectProvider** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="7aa73-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7aa73-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7aa73-131">-Confirm</span></span>
<span data-ttu-id="7aa73-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7aa73-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aa73-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aa73-133">-WhatIf</span></span>
<span data-ttu-id="7aa73-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7aa73-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7aa73-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7aa73-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aa73-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa73-136">CommonParameters</span></span>
<span data-ttu-id="7aa73-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aa73-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa73-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7aa73-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa73-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7aa73-139">INPUTS</span></span>

### <span data-ttu-id="7aa73-140">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7aa73-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7aa73-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7aa73-141">System.String</span></span>

### <span data-ttu-id="7aa73-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7aa73-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7aa73-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7aa73-143">OUTPUTS</span></span>

### <span data-ttu-id="7aa73-144">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="7aa73-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="7aa73-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7aa73-145">NOTES</span></span>

## <span data-ttu-id="7aa73-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7aa73-146">RELATED LINKS</span></span>

[<span data-ttu-id="7aa73-147">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="7aa73-147">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="7aa73-148">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="7aa73-148">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="7aa73-149">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="7aa73-149">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


