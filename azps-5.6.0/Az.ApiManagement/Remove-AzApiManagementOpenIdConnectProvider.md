---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 3d7d6600e7e26202c920499a615f4124767c830c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890024"
---
# <span data-ttu-id="4acc0-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4acc0-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="4acc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4acc0-102">SYNOPSIS</span></span>
<span data-ttu-id="4acc0-103">Remove um provedor do OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="4acc0-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="4acc0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4acc0-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4acc0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4acc0-105">DESCRIPTION</span></span>
<span data-ttu-id="4acc0-106">O cmdlet **Remove-AzApiManagementOpenIdConnectProvider** remove um provedor de Conexão OpenID para o Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="4acc0-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="4acc0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4acc0-107">EXAMPLES</span></span>

### <span data-ttu-id="4acc0-108">Exemplo 1: Remover um provedor</span><span class="sxs-lookup"><span data-stu-id="4acc0-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="4acc0-109">Este comando remove um provedor que tem a ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="4acc0-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="4acc0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4acc0-110">PARAMETERS</span></span>

### <span data-ttu-id="4acc0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4acc0-111">-Context</span></span>
<span data-ttu-id="4acc0-112">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="4acc0-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4acc0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4acc0-113">-DefaultProfile</span></span>
<span data-ttu-id="4acc0-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4acc0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4acc0-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="4acc0-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="4acc0-116">Especifica uma ID do provedor que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="4acc0-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4acc0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4acc0-117">-PassThru</span></span>
<span data-ttu-id="4acc0-118">Indica que esse cmdlet retornará um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="4acc0-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="4acc0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4acc0-119">-Confirm</span></span>
<span data-ttu-id="4acc0-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4acc0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4acc0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4acc0-121">-WhatIf</span></span>
<span data-ttu-id="4acc0-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4acc0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4acc0-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4acc0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4acc0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4acc0-124">CommonParameters</span></span>
<span data-ttu-id="4acc0-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4acc0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4acc0-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4acc0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4acc0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4acc0-127">INPUTS</span></span>

### <span data-ttu-id="4acc0-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4acc0-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4acc0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4acc0-129">System.String</span></span>

### <span data-ttu-id="4acc0-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4acc0-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4acc0-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4acc0-131">OUTPUTS</span></span>

### <span data-ttu-id="4acc0-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4acc0-132">System.Boolean</span></span>

## <span data-ttu-id="4acc0-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="4acc0-133">NOTES</span></span>

## <span data-ttu-id="4acc0-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4acc0-134">RELATED LINKS</span></span>

[<span data-ttu-id="4acc0-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4acc0-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="4acc0-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4acc0-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="4acc0-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4acc0-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


