---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
ms.openlocfilehash: 323cbbdc38281c9b90ab3728eb2879bf1b7bfe89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597969"
---
# <span data-ttu-id="ac8bc-101">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ac8bc-101">Remove-AzApiManagementProperty</span></span>

## <span data-ttu-id="ac8bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8bc-103">Remove uma propriedade de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="ac8bc-103">Removes an API Management Property.</span></span>

## <span data-ttu-id="ac8bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac8bc-104">SYNTAX</span></span>

```
Remove-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac8bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac8bc-105">DESCRIPTION</span></span>
<span data-ttu-id="ac8bc-106">O cmdlet **Remove-AzApiManagementProperty** remove uma **Propriedade** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="ac8bc-106">The **Remove-AzApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="ac8bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac8bc-107">EXAMPLES</span></span>

### <span data-ttu-id="ac8bc-108">Exemplo 1: remover uma propriedade</span><span class="sxs-lookup"><span data-stu-id="ac8bc-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="ac8bc-109">Esse comando Remove a propriedade que tem a ID Property11.</span><span class="sxs-lookup"><span data-stu-id="ac8bc-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="ac8bc-110">OS</span><span class="sxs-lookup"><span data-stu-id="ac8bc-110">PARAMETERS</span></span>

### <span data-ttu-id="ac8bc-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ac8bc-111">-Context</span></span>
<span data-ttu-id="ac8bc-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ac8bc-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ac8bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8bc-113">-DefaultProfile</span></span>
<span data-ttu-id="ac8bc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac8bc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac8bc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac8bc-115">-PassThru</span></span>
<span data-ttu-id="ac8bc-116">Indica que esse cmdlet retorna um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ac8bc-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="ac8bc-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="ac8bc-117">-PropertyId</span></span>
<span data-ttu-id="ac8bc-118">Especifica uma ID da propriedade que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ac8bc-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ac8bc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ac8bc-119">-Confirm</span></span>
<span data-ttu-id="ac8bc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac8bc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac8bc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac8bc-121">-WhatIf</span></span>
<span data-ttu-id="ac8bc-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ac8bc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac8bc-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac8bc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac8bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8bc-124">CommonParameters</span></span>
<span data-ttu-id="ac8bc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac8bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8bc-126">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac8bc-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8bc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac8bc-127">INPUTS</span></span>

### <span data-ttu-id="ac8bc-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ac8bc-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ac8bc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ac8bc-129">System.String</span></span>

### <span data-ttu-id="ac8bc-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ac8bc-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ac8bc-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac8bc-131">OUTPUTS</span></span>

### <span data-ttu-id="ac8bc-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac8bc-132">System.Boolean</span></span>

## <span data-ttu-id="ac8bc-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac8bc-133">NOTES</span></span>

## <span data-ttu-id="ac8bc-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac8bc-134">RELATED LINKS</span></span>

[<span data-ttu-id="ac8bc-135">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ac8bc-135">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="ac8bc-136">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="ac8bc-136">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


