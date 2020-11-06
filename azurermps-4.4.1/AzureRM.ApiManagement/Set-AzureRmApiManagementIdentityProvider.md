---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 76ee402fee2e18d426875340d4eaadda2cc63042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431842"
---
# <span data-ttu-id="456d8-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="456d8-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="456d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="456d8-102">SYNOPSIS</span></span>
<span data-ttu-id="456d8-103">Atualiza a configuração de um provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="456d8-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="456d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="456d8-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="456d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="456d8-105">DESCRIPTION</span></span>
<span data-ttu-id="456d8-106">Atualiza a configuração de um provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="456d8-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="456d8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="456d8-107">EXAMPLES</span></span>

### <span data-ttu-id="456d8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="456d8-108">Example 1</span></span>
```
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimcontext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="456d8-109">O cmdlet atualiza o segredo do cliente do provedor de identidade do Facebook;</span><span class="sxs-lookup"><span data-stu-id="456d8-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="456d8-110">OS</span><span class="sxs-lookup"><span data-stu-id="456d8-110">PARAMETERS</span></span>

### <span data-ttu-id="456d8-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="456d8-111">-AllowedTenants</span></span>
<span data-ttu-id="456d8-112">Lista de locatários do Azure Active Directory permitidos.</span><span class="sxs-lookup"><span data-stu-id="456d8-112">List of allowed Azure Active Directory Tenants.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="456d8-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="456d8-113">-ClientId</span></span>
<span data-ttu-id="456d8-114">ID do cliente do aplicativo no provedor de identidade externa.</span><span class="sxs-lookup"><span data-stu-id="456d8-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="456d8-115">Ele é uma ID do aplicativo para o logon do Facebook, ID de cliente para o Google login, ID do aplicativo para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="456d8-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="456d8-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="456d8-116">-ClientSecret</span></span>
<span data-ttu-id="456d8-117">Segredo do cliente do aplicativo no provedor de identidade externa, usado para autenticar a solicitação de logon.</span><span class="sxs-lookup"><span data-stu-id="456d8-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="456d8-118">Por exemplo, é o segredo do aplicativo para o logon do Facebook, a chave de API do Google login, a chave pública para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="456d8-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="456d8-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="456d8-119">-Context</span></span>
<span data-ttu-id="456d8-120">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="456d8-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="456d8-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="456d8-121">This parameter is required.</span></span>

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

### <span data-ttu-id="456d8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="456d8-122">-PassThru</span></span>
<span data-ttu-id="456d8-123">Indica que esse cmdlet retorna o  **PsApiManagementIdentityProvider** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="456d8-123">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


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

### <span data-ttu-id="456d8-124">-Digite</span><span class="sxs-lookup"><span data-stu-id="456d8-124">-Type</span></span>
<span data-ttu-id="456d8-125">Identificador de um provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="456d8-125">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="456d8-126">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="456d8-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="456d8-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="456d8-127">-Confirm</span></span>
<span data-ttu-id="456d8-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="456d8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="456d8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="456d8-129">-WhatIf</span></span>
<span data-ttu-id="456d8-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="456d8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="456d8-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="456d8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="456d8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="456d8-132">-DefaultProfile</span></span>
<span data-ttu-id="456d8-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="456d8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="456d8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456d8-134">CommonParameters</span></span>
<span data-ttu-id="456d8-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="456d8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456d8-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="456d8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456d8-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="456d8-137">INPUTS</span></span>

## <span data-ttu-id="456d8-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="456d8-138">OUTPUTS</span></span>

### <span data-ttu-id="456d8-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="456d8-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="456d8-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="456d8-140">NOTES</span></span>

## <span data-ttu-id="456d8-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="456d8-141">RELATED LINKS</span></span>

[<span data-ttu-id="456d8-142">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="456d8-142">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="456d8-143">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="456d8-143">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="456d8-144">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="456d8-144">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
