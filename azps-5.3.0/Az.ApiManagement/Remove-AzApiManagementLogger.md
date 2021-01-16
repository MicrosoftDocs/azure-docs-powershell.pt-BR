---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: e68fec8bf38dc990737f11d5dc3ed079d71fd6ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272154"
---
# <span data-ttu-id="3e060-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3e060-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="3e060-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e060-102">SYNOPSIS</span></span>
<span data-ttu-id="3e060-103">Remove um agente de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="3e060-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="3e060-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e060-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e060-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e060-105">DESCRIPTION</span></span>
<span data-ttu-id="3e060-106">O cmdlet **Remove-AzApiManagementLogger** remove um **agente** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e060-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="3e060-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e060-107">EXAMPLES</span></span>

### <span data-ttu-id="3e060-108">Exemplo 1: remover um agente de log</span><span class="sxs-lookup"><span data-stu-id="3e060-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="3e060-109">Esse comando Remove um logger que tem a ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="3e060-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="3e060-110">OS</span><span class="sxs-lookup"><span data-stu-id="3e060-110">PARAMETERS</span></span>

### <span data-ttu-id="3e060-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3e060-111">-Context</span></span>
<span data-ttu-id="3e060-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3e060-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3e060-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e060-113">-DefaultProfile</span></span>
<span data-ttu-id="3e060-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e060-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e060-115">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="3e060-115">-LoggerId</span></span>
<span data-ttu-id="3e060-116">Especifica a ID do agente de log a ser removida.</span><span class="sxs-lookup"><span data-stu-id="3e060-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="3e060-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e060-117">-PassThru</span></span>
<span data-ttu-id="3e060-118">Indica que esse cmdlet retorna um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3e060-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="3e060-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e060-119">-Confirm</span></span>
<span data-ttu-id="3e060-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e060-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e060-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e060-121">-WhatIf</span></span>
<span data-ttu-id="3e060-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3e060-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e060-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e060-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e060-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e060-124">CommonParameters</span></span>
<span data-ttu-id="3e060-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e060-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e060-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e060-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e060-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e060-127">INPUTS</span></span>

### <span data-ttu-id="3e060-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3e060-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3e060-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3e060-129">System.String</span></span>

### <span data-ttu-id="3e060-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3e060-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3e060-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e060-131">OUTPUTS</span></span>

### <span data-ttu-id="3e060-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e060-132">System.Boolean</span></span>

## <span data-ttu-id="3e060-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e060-133">NOTES</span></span>

## <span data-ttu-id="3e060-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e060-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e060-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3e060-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="3e060-136">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3e060-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="3e060-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3e060-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


