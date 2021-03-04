---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: 7bdf37996fb5d407d3961ddacee4701acce2baaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885503"
---
# <span data-ttu-id="32d96-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="32d96-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="32d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32d96-102">SYNOPSIS</span></span>
<span data-ttu-id="32d96-103">Remove um Api Management Logger.</span><span class="sxs-lookup"><span data-stu-id="32d96-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="32d96-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="32d96-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32d96-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="32d96-105">DESCRIPTION</span></span>
<span data-ttu-id="32d96-106">O cmdlet **Remove-AzApiManagementLogger** remove um Azure API Management **Logger**.</span><span class="sxs-lookup"><span data-stu-id="32d96-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="32d96-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32d96-107">EXAMPLES</span></span>

### <span data-ttu-id="32d96-108">Exemplo 1: Remover um madeireiro</span><span class="sxs-lookup"><span data-stu-id="32d96-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="32d96-109">Este comando remove um madeireiro que tem o ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="32d96-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="32d96-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="32d96-110">PARAMETERS</span></span>

### <span data-ttu-id="32d96-111">-Context</span><span class="sxs-lookup"><span data-stu-id="32d96-111">-Context</span></span>
<span data-ttu-id="32d96-112">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="32d96-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="32d96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d96-113">-DefaultProfile</span></span>
<span data-ttu-id="32d96-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="32d96-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32d96-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="32d96-115">-LoggerId</span></span>
<span data-ttu-id="32d96-116">Especifica a ID do madeireiro a ser removido.</span><span class="sxs-lookup"><span data-stu-id="32d96-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="32d96-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32d96-117">-PassThru</span></span>
<span data-ttu-id="32d96-118">Indica que esse cmdlet retornará um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="32d96-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="32d96-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32d96-119">-Confirm</span></span>
<span data-ttu-id="32d96-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32d96-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32d96-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32d96-121">-WhatIf</span></span>
<span data-ttu-id="32d96-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32d96-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32d96-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32d96-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32d96-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d96-124">CommonParameters</span></span>
<span data-ttu-id="32d96-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32d96-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d96-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32d96-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d96-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32d96-127">INPUTS</span></span>

### <span data-ttu-id="32d96-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="32d96-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="32d96-129">System.String</span><span class="sxs-lookup"><span data-stu-id="32d96-129">System.String</span></span>

### <span data-ttu-id="32d96-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="32d96-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="32d96-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="32d96-131">OUTPUTS</span></span>

### <span data-ttu-id="32d96-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="32d96-132">System.Boolean</span></span>

## <span data-ttu-id="32d96-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="32d96-133">NOTES</span></span>

## <span data-ttu-id="32d96-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32d96-134">RELATED LINKS</span></span>

[<span data-ttu-id="32d96-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="32d96-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="32d96-136">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="32d96-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="32d96-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="32d96-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


