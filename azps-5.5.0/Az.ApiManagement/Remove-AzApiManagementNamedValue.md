---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116649"
---
# <span data-ttu-id="2e56b-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="2e56b-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="2e56b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e56b-102">SYNOPSIS</span></span>
<span data-ttu-id="2e56b-103">Remove um valor nomeado de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2e56b-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="2e56b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e56b-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e56b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e56b-105">DESCRIPTION</span></span>
<span data-ttu-id="2e56b-106">O cmdlet **Remove-AzApiManagementNamedValue** remove um valor nomeado de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e56b-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="2e56b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2e56b-107">EXAMPLES</span></span>

### <span data-ttu-id="2e56b-108">Exemplo 1: remover o valor nomeado</span><span class="sxs-lookup"><span data-stu-id="2e56b-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="2e56b-109">Esse comando remove o valor nomeado que tem a Propriedade ID11.</span><span class="sxs-lookup"><span data-stu-id="2e56b-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="2e56b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e56b-110">PARAMETERS</span></span>

### <span data-ttu-id="2e56b-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2e56b-111">-Context</span></span>
<span data-ttu-id="2e56b-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2e56b-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2e56b-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="2e56b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2e56b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e56b-114">-DefaultProfile</span></span>
<span data-ttu-id="2e56b-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e56b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e56b-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="2e56b-116">-NamedValueId</span></span>
<span data-ttu-id="2e56b-117">Identificador de valor nomeado existente.</span><span class="sxs-lookup"><span data-stu-id="2e56b-117">Identifier of existing named value.</span></span>
<span data-ttu-id="2e56b-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="2e56b-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2e56b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e56b-119">-PassThru</span></span>
<span data-ttu-id="2e56b-120">Se especificado, a gravação será verdadeira caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2e56b-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2e56b-121">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2e56b-121">This parameter is optional.</span></span>
<span data-ttu-id="2e56b-122">O valor padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="2e56b-122">Default value is false.</span></span>

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

### <span data-ttu-id="2e56b-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2e56b-123">-Confirm</span></span>
<span data-ttu-id="2e56b-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e56b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e56b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e56b-125">-WhatIf</span></span>
<span data-ttu-id="2e56b-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2e56b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e56b-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e56b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e56b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e56b-128">CommonParameters</span></span>
<span data-ttu-id="2e56b-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e56b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e56b-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e56b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e56b-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="2e56b-131">INPUTS</span></span>

### <span data-ttu-id="2e56b-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e56b-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e56b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2e56b-133">System.String</span></span>

### <span data-ttu-id="2e56b-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e56b-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2e56b-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="2e56b-135">OUTPUTS</span></span>

### <span data-ttu-id="2e56b-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e56b-136">System.Boolean</span></span>

## <span data-ttu-id="2e56b-137">Notas</span><span class="sxs-lookup"><span data-stu-id="2e56b-137">NOTES</span></span>

## <span data-ttu-id="2e56b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e56b-138">RELATED LINKS</span></span>
