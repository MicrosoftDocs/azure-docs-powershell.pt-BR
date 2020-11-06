---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f890236907ea0a717245d9345be276a6ccf04b8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431831"
---
# <span data-ttu-id="f8e68-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f8e68-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f8e68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8e68-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e68-103">Modifica um provedor OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="f8e68-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8e68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8e68-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8e68-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8e68-105">DESCRIPTION</span></span>
<span data-ttu-id="f8e68-106">O cmdlet **set-AzureRmApiManagementOpenIdConnectProvider** modifica um provedor de conexão OpenID no gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8e68-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="f8e68-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8e68-107">EXAMPLES</span></span>

### <span data-ttu-id="f8e68-108">Exemplo 1: alterar o segredo do cliente para um provedor</span><span class="sxs-lookup"><span data-stu-id="f8e68-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="f8e68-109">Esse comando modifica o provedor que tem a ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="f8e68-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="f8e68-110">O comando especifica um segredo do cliente para o provedor.</span><span class="sxs-lookup"><span data-stu-id="f8e68-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="f8e68-111">OS</span><span class="sxs-lookup"><span data-stu-id="f8e68-111">PARAMETERS</span></span>

### <span data-ttu-id="f8e68-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="f8e68-112">-ClientId</span></span>
<span data-ttu-id="f8e68-113">Especifica a ID do cliente do console de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="f8e68-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="f8e68-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="f8e68-114">-ClientSecret</span></span>
<span data-ttu-id="f8e68-115">Especifica o segredo do cliente do console de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="f8e68-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="f8e68-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f8e68-116">-Context</span></span>
<span data-ttu-id="f8e68-117">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f8e68-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f8e68-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f8e68-118">-Description</span></span>
<span data-ttu-id="f8e68-119">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="f8e68-119">Specifies a description.</span></span>

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

### <span data-ttu-id="f8e68-120">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="f8e68-120">-MetadataEndpointUri</span></span>
<span data-ttu-id="f8e68-121">Especifica um URI de ponto de extremidade de metadados do provedor.</span><span class="sxs-lookup"><span data-stu-id="f8e68-121">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="f8e68-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8e68-122">-Name</span></span>
<span data-ttu-id="f8e68-123">Especifica um nome amigável para o provedor.</span><span class="sxs-lookup"><span data-stu-id="f8e68-123">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="f8e68-124">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="f8e68-124">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="f8e68-125">Especifica uma ID para o provedor que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="f8e68-125">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="f8e68-126">Se você não especificar uma ID, esse cmdlet gerará uma.</span><span class="sxs-lookup"><span data-stu-id="f8e68-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="f8e68-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8e68-127">-PassThru</span></span>
<span data-ttu-id="f8e68-128">Indica que esse cmdlet retorna o **PsApiManagementOpenIdConnectProvider** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="f8e68-128">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f8e68-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e68-129">-DefaultProfile</span></span>
<span data-ttu-id="f8e68-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8e68-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8e68-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e68-131">CommonParameters</span></span>
<span data-ttu-id="f8e68-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8e68-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e68-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e68-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e68-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8e68-134">INPUTS</span></span>

## <span data-ttu-id="f8e68-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8e68-135">OUTPUTS</span></span>

### <span data-ttu-id="f8e68-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f8e68-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f8e68-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8e68-137">NOTES</span></span>

## <span data-ttu-id="f8e68-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8e68-138">RELATED LINKS</span></span>

[<span data-ttu-id="f8e68-139">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f8e68-139">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f8e68-140">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f8e68-140">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f8e68-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f8e68-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


