---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6b4ccac87f963f9948c67d3162f1677b9860583b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426482"
---
# <span data-ttu-id="722a0-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="722a0-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="722a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="722a0-102">SYNOPSIS</span></span>
<span data-ttu-id="722a0-103">Remove um provedor OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="722a0-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="722a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="722a0-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="722a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="722a0-105">DESCRIPTION</span></span>
<span data-ttu-id="722a0-106">O cmdlet **Remove-AzureRmApiManagementOpenIdConnectProvider** remove um provedor OpenID Connect para o gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="722a0-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="722a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="722a0-107">EXAMPLES</span></span>

### <span data-ttu-id="722a0-108">Exemplo 1: remover um provedor</span><span class="sxs-lookup"><span data-stu-id="722a0-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="722a0-109">Esse comando Remove um provedor que tem a ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="722a0-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="722a0-110">OS</span><span class="sxs-lookup"><span data-stu-id="722a0-110">PARAMETERS</span></span>

### <span data-ttu-id="722a0-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="722a0-111">-Context</span></span>
<span data-ttu-id="722a0-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="722a0-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="722a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="722a0-113">-DefaultProfile</span></span>
<span data-ttu-id="722a0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="722a0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="722a0-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="722a0-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="722a0-116">Especifica uma ID do provedor que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="722a0-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="722a0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="722a0-117">-PassThru</span></span>
<span data-ttu-id="722a0-118">Indica que esse cmdlet retorna um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="722a0-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="722a0-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="722a0-119">-Confirm</span></span>
<span data-ttu-id="722a0-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="722a0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="722a0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="722a0-121">-WhatIf</span></span>
<span data-ttu-id="722a0-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="722a0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="722a0-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="722a0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="722a0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="722a0-124">CommonParameters</span></span>
<span data-ttu-id="722a0-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="722a0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="722a0-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="722a0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="722a0-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="722a0-127">INPUTS</span></span>

### <span data-ttu-id="722a0-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="722a0-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="722a0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="722a0-129">System.String</span></span>

### <span data-ttu-id="722a0-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="722a0-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="722a0-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="722a0-131">OUTPUTS</span></span>

### <span data-ttu-id="722a0-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="722a0-132">System.Boolean</span></span>

## <span data-ttu-id="722a0-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="722a0-133">NOTES</span></span>

## <span data-ttu-id="722a0-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="722a0-134">RELATED LINKS</span></span>

[<span data-ttu-id="722a0-135">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="722a0-135">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="722a0-136">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="722a0-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="722a0-137">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="722a0-137">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


