---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954481"
---
# <span data-ttu-id="bc0e6-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bc0e6-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bc0e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc0e6-102">SYNOPSIS</span></span>
<span data-ttu-id="bc0e6-103">Remove um provedor OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="bc0e6-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="bc0e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc0e6-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc0e6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc0e6-105">DESCRIPTION</span></span>
<span data-ttu-id="bc0e6-106">O cmdlet **Remove-AzApiManagementOpenIdConnectProvider** remove um provedor OpenID Connect para o gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0e6-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="bc0e6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc0e6-107">EXAMPLES</span></span>

### <span data-ttu-id="bc0e6-108">Exemplo 1: remover um provedor</span><span class="sxs-lookup"><span data-stu-id="bc0e6-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="bc0e6-109">Esse comando Remove um provedor que tem a ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="bc0e6-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="bc0e6-110">OS</span><span class="sxs-lookup"><span data-stu-id="bc0e6-110">PARAMETERS</span></span>

### <span data-ttu-id="bc0e6-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="bc0e6-111">-Context</span></span>
<span data-ttu-id="bc0e6-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="bc0e6-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bc0e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc0e6-113">-DefaultProfile</span></span>
<span data-ttu-id="bc0e6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0e6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc0e6-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="bc0e6-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="bc0e6-116">Especifica uma ID do provedor que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="bc0e6-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bc0e6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc0e6-117">-PassThru</span></span>
<span data-ttu-id="bc0e6-118">Indica que esse cmdlet retorna um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="bc0e6-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="bc0e6-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bc0e6-119">-Confirm</span></span>
<span data-ttu-id="bc0e6-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc0e6-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc0e6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc0e6-121">-WhatIf</span></span>
<span data-ttu-id="bc0e6-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc0e6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc0e6-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc0e6-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc0e6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc0e6-124">CommonParameters</span></span>
<span data-ttu-id="bc0e6-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc0e6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc0e6-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc0e6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc0e6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc0e6-127">INPUTS</span></span>

### <span data-ttu-id="bc0e6-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bc0e6-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bc0e6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bc0e6-129">System.String</span></span>

### <span data-ttu-id="bc0e6-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bc0e6-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bc0e6-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc0e6-131">OUTPUTS</span></span>

### <span data-ttu-id="bc0e6-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc0e6-132">System.Boolean</span></span>

## <span data-ttu-id="bc0e6-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc0e6-133">NOTES</span></span>

## <span data-ttu-id="bc0e6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc0e6-134">RELATED LINKS</span></span>

[<span data-ttu-id="bc0e6-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bc0e6-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bc0e6-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bc0e6-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bc0e6-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bc0e6-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


