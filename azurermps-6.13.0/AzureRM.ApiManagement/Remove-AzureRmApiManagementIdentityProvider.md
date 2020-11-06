---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d8cc54570b1282889a93c803e1216096cde35b27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426485"
---
# <span data-ttu-id="db6e4-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="db6e4-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="db6e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db6e4-102">SYNOPSIS</span></span>
<span data-ttu-id="db6e4-103">Remove uma configuração de provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="db6e4-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db6e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db6e4-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db6e4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db6e4-105">DESCRIPTION</span></span>
<span data-ttu-id="db6e4-106">Remove uma configuração de provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="db6e4-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="db6e4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db6e4-107">EXAMPLES</span></span>

### <span data-ttu-id="db6e4-108">Remove as configurações do provedor de identidade do Facebook do serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db6e4-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="db6e4-109">Exclui a configuração relacionada à configuração do provedor de identidade do Facebook.</span><span class="sxs-lookup"><span data-stu-id="db6e4-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="db6e4-110">OS</span><span class="sxs-lookup"><span data-stu-id="db6e4-110">PARAMETERS</span></span>

### <span data-ttu-id="db6e4-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="db6e4-111">-Context</span></span>
<span data-ttu-id="db6e4-112">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="db6e4-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="db6e4-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="db6e4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="db6e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6e4-114">-DefaultProfile</span></span>
<span data-ttu-id="db6e4-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db6e4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db6e4-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db6e4-116">-PassThru</span></span>
<span data-ttu-id="db6e4-117">Indica que esse cmdlet retorna um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="db6e4-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="db6e4-118">-Digite</span><span class="sxs-lookup"><span data-stu-id="db6e4-118">-Type</span></span>
<span data-ttu-id="db6e4-119">Identificador de um provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="db6e4-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="db6e4-120">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="db6e4-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db6e4-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db6e4-121">-Confirm</span></span>
<span data-ttu-id="db6e4-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db6e4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db6e4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db6e4-123">-WhatIf</span></span>
<span data-ttu-id="db6e4-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db6e4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db6e4-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db6e4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db6e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6e4-126">CommonParameters</span></span>
<span data-ttu-id="db6e4-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6e4-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6e4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6e4-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db6e4-129">INPUTS</span></span>

### <span data-ttu-id="db6e4-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="db6e4-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="db6e4-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="db6e4-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="db6e4-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="db6e4-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="db6e4-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db6e4-133">OUTPUTS</span></span>

### <span data-ttu-id="db6e4-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db6e4-134">System.Boolean</span></span>

## <span data-ttu-id="db6e4-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db6e4-135">NOTES</span></span>

## <span data-ttu-id="db6e4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db6e4-136">RELATED LINKS</span></span>

[<span data-ttu-id="db6e4-137">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="db6e4-137">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="db6e4-138">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="db6e4-138">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="db6e4-139">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="db6e4-139">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

