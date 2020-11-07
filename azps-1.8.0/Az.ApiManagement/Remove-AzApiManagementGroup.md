---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 89ea2d36e3b3b65c08e6a053d402f9be4966a738
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771380"
---
# <span data-ttu-id="15185-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="15185-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="15185-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15185-102">SYNOPSIS</span></span>
<span data-ttu-id="15185-103">Remove um grupo de gerenciamento de APIs existente.</span><span class="sxs-lookup"><span data-stu-id="15185-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="15185-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15185-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15185-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15185-105">DESCRIPTION</span></span>
<span data-ttu-id="15185-106">O cmdlet **Remove-AzApiManagementGroup** remove um grupo de gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="15185-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="15185-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15185-107">EXAMPLES</span></span>

### <span data-ttu-id="15185-108">Exemplo 1: remover um grupo de gerenciamento existente</span><span class="sxs-lookup"><span data-stu-id="15185-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="15185-109">Esse comando Remove um grupo de gerenciamento existente chamado Group0001 e não solicita que o usuário confirme.</span><span class="sxs-lookup"><span data-stu-id="15185-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="15185-110">OS</span><span class="sxs-lookup"><span data-stu-id="15185-110">PARAMETERS</span></span>

### <span data-ttu-id="15185-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="15185-111">-Context</span></span>
<span data-ttu-id="15185-112">Especifica a instância de um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="15185-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="15185-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15185-113">-DefaultProfile</span></span>
<span data-ttu-id="15185-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15185-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15185-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="15185-115">-GroupId</span></span>
<span data-ttu-id="15185-116">Especifica o identificador de um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="15185-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="15185-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15185-117">-PassThru</span></span>
<span data-ttu-id="15185-118">Indica que esse cmdlet retorna um valor de $True se tiver êxito ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="15185-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="15185-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="15185-119">-Confirm</span></span>
<span data-ttu-id="15185-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15185-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15185-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15185-121">-WhatIf</span></span>
<span data-ttu-id="15185-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15185-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15185-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15185-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15185-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15185-124">CommonParameters</span></span>
<span data-ttu-id="15185-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15185-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15185-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15185-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15185-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15185-127">INPUTS</span></span>

### <span data-ttu-id="15185-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="15185-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="15185-129">System. String</span><span class="sxs-lookup"><span data-stu-id="15185-129">System.String</span></span>

### <span data-ttu-id="15185-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="15185-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="15185-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15185-131">OUTPUTS</span></span>

### <span data-ttu-id="15185-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15185-132">System.Boolean</span></span>

## <span data-ttu-id="15185-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15185-133">NOTES</span></span>

## <span data-ttu-id="15185-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15185-134">RELATED LINKS</span></span>

[<span data-ttu-id="15185-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="15185-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="15185-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="15185-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="15185-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="15185-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


