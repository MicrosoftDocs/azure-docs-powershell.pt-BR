---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 135dced6c66f1212f172a2c435a7468b16e71708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426486"
---
# <span data-ttu-id="2e34f-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2e34f-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="2e34f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e34f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e34f-103">Remove um agente de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2e34f-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e34f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e34f-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e34f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e34f-105">DESCRIPTION</span></span>
<span data-ttu-id="2e34f-106">O cmdlet **Remove-AzureRmApiManagementLogger** remove um **agente** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e34f-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="2e34f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e34f-107">EXAMPLES</span></span>

### <span data-ttu-id="2e34f-108">Exemplo 1: remover um agente de log</span><span class="sxs-lookup"><span data-stu-id="2e34f-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="2e34f-109">Esse comando Remove um logger que tem a ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="2e34f-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="2e34f-110">OS</span><span class="sxs-lookup"><span data-stu-id="2e34f-110">PARAMETERS</span></span>

### <span data-ttu-id="2e34f-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2e34f-111">-Context</span></span>
<span data-ttu-id="2e34f-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2e34f-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2e34f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e34f-113">-DefaultProfile</span></span>
<span data-ttu-id="2e34f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e34f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e34f-115">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="2e34f-115">-LoggerId</span></span>
<span data-ttu-id="2e34f-116">Especifica a ID do agente de log a ser removida.</span><span class="sxs-lookup"><span data-stu-id="2e34f-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="2e34f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e34f-117">-PassThru</span></span>
<span data-ttu-id="2e34f-118">Indica que esse cmdlet retorna um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="2e34f-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="2e34f-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e34f-119">-Confirm</span></span>
<span data-ttu-id="2e34f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e34f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e34f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e34f-121">-WhatIf</span></span>
<span data-ttu-id="2e34f-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e34f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e34f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e34f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e34f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e34f-124">CommonParameters</span></span>
<span data-ttu-id="2e34f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e34f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e34f-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e34f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e34f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e34f-127">INPUTS</span></span>

### <span data-ttu-id="2e34f-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e34f-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e34f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2e34f-129">System.String</span></span>

### <span data-ttu-id="2e34f-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e34f-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2e34f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e34f-131">OUTPUTS</span></span>

### <span data-ttu-id="2e34f-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2e34f-132">System.Boolean</span></span>

## <span data-ttu-id="2e34f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e34f-133">NOTES</span></span>

## <span data-ttu-id="2e34f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e34f-134">RELATED LINKS</span></span>

[<span data-ttu-id="2e34f-135">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2e34f-135">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="2e34f-136">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2e34f-136">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="2e34f-137">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2e34f-137">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)

