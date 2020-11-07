---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 5258b041f2858ce766f5b6e932412986545ccf13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771379"
---
# <span data-ttu-id="a0c18-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a0c18-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="a0c18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0c18-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c18-103">Remove uma configuração de provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="a0c18-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="a0c18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0c18-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0c18-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0c18-105">DESCRIPTION</span></span>
<span data-ttu-id="a0c18-106">Remove uma configuração de provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="a0c18-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="a0c18-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0c18-107">EXAMPLES</span></span>

### <span data-ttu-id="a0c18-108">Remove as configurações do provedor de identidade do Facebook do serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a0c18-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="a0c18-109">Exclui a configuração relacionada à configuração do provedor de identidade do Facebook.</span><span class="sxs-lookup"><span data-stu-id="a0c18-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="a0c18-110">OS</span><span class="sxs-lookup"><span data-stu-id="a0c18-110">PARAMETERS</span></span>

### <span data-ttu-id="a0c18-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a0c18-111">-Context</span></span>
<span data-ttu-id="a0c18-112">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a0c18-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a0c18-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a0c18-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a0c18-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c18-114">-DefaultProfile</span></span>
<span data-ttu-id="a0c18-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0c18-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0c18-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0c18-116">-PassThru</span></span>
<span data-ttu-id="a0c18-117">Indica que esse cmdlet retorna um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="a0c18-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="a0c18-118">-Digite</span><span class="sxs-lookup"><span data-stu-id="a0c18-118">-Type</span></span>
<span data-ttu-id="a0c18-119">Identificador de um provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="a0c18-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="a0c18-120">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a0c18-120">This parameter is required.</span></span>

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

### <span data-ttu-id="a0c18-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a0c18-121">-Confirm</span></span>
<span data-ttu-id="a0c18-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0c18-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0c18-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0c18-123">-WhatIf</span></span>
<span data-ttu-id="a0c18-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0c18-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0c18-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0c18-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0c18-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c18-126">CommonParameters</span></span>
<span data-ttu-id="a0c18-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0c18-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c18-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0c18-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c18-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0c18-129">INPUTS</span></span>

### <span data-ttu-id="a0c18-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a0c18-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a0c18-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="a0c18-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="a0c18-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a0c18-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a0c18-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0c18-133">OUTPUTS</span></span>

### <span data-ttu-id="a0c18-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0c18-134">System.Boolean</span></span>

## <span data-ttu-id="a0c18-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0c18-135">NOTES</span></span>

## <span data-ttu-id="a0c18-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0c18-136">RELATED LINKS</span></span>

[<span data-ttu-id="a0c18-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a0c18-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="a0c18-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a0c18-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="a0c18-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a0c18-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

