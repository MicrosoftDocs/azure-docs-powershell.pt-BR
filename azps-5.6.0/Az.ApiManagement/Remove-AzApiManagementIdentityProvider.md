---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f80fe2b09be6d4bdc624f65de014d3b7f1beadd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901517"
---
# <span data-ttu-id="df1d1-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="df1d1-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="df1d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="df1d1-103">Remove uma configuração existente do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="df1d1-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="df1d1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="df1d1-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df1d1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="df1d1-105">DESCRIPTION</span></span>
<span data-ttu-id="df1d1-106">Remove uma configuração existente do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="df1d1-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="df1d1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df1d1-107">EXAMPLES</span></span>

### <span data-ttu-id="df1d1-108">Exemplo 1: remove as configurações do provedor de identidade do Facebook do serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="df1d1-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="df1d1-109">Exclui a configuração relacionada à configuração do provedor de Identidade do Facebook.</span><span class="sxs-lookup"><span data-stu-id="df1d1-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="df1d1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="df1d1-110">PARAMETERS</span></span>

### <span data-ttu-id="df1d1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="df1d1-111">-Context</span></span>
<span data-ttu-id="df1d1-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="df1d1-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="df1d1-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="df1d1-113">This parameter is required.</span></span>

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

### <span data-ttu-id="df1d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1d1-114">-DefaultProfile</span></span>
<span data-ttu-id="df1d1-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="df1d1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df1d1-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df1d1-116">-PassThru</span></span>
<span data-ttu-id="df1d1-117">Indica que esse cmdlet retornará um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="df1d1-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="df1d1-118">-Type</span><span class="sxs-lookup"><span data-stu-id="df1d1-118">-Type</span></span>
<span data-ttu-id="df1d1-119">Identificador de um Provedor de Identidade existente.</span><span class="sxs-lookup"><span data-stu-id="df1d1-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="df1d1-120">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="df1d1-120">This parameter is required.</span></span>

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

### <span data-ttu-id="df1d1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df1d1-121">-Confirm</span></span>
<span data-ttu-id="df1d1-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df1d1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df1d1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df1d1-123">-WhatIf</span></span>
<span data-ttu-id="df1d1-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df1d1-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df1d1-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df1d1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df1d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1d1-126">CommonParameters</span></span>
<span data-ttu-id="df1d1-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df1d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1d1-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df1d1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1d1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df1d1-129">INPUTS</span></span>

### <span data-ttu-id="df1d1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="df1d1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="df1d1-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="df1d1-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="df1d1-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="df1d1-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="df1d1-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="df1d1-133">OUTPUTS</span></span>

### <span data-ttu-id="df1d1-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df1d1-134">System.Boolean</span></span>

## <span data-ttu-id="df1d1-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="df1d1-135">NOTES</span></span>

## <span data-ttu-id="df1d1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df1d1-136">RELATED LINKS</span></span>

[<span data-ttu-id="df1d1-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="df1d1-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="df1d1-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="df1d1-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="df1d1-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="df1d1-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

