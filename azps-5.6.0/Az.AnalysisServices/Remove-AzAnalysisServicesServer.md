---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: 782fcae5d243a1686e20237843d69b02564755f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892577"
---
# <span data-ttu-id="6754f-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6754f-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="6754f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6754f-102">SYNOPSIS</span></span>
<span data-ttu-id="6754f-103">Exclui uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6754f-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="6754f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6754f-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6754f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6754f-105">DESCRIPTION</span></span>
<span data-ttu-id="6754f-106">O Remove-AzAnalysisServicesServer cmdlet exclui uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6754f-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="6754f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6754f-107">EXAMPLES</span></span>

### <span data-ttu-id="6754f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6754f-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="6754f-109">Este comando removerá o servidor chamado testserver no grupo de recursos testgroup</span><span class="sxs-lookup"><span data-stu-id="6754f-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="6754f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6754f-110">PARAMETERS</span></span>

### <span data-ttu-id="6754f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6754f-111">-DefaultProfile</span></span>
<span data-ttu-id="6754f-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6754f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6754f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6754f-113">-Name</span></span>
<span data-ttu-id="6754f-114">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6754f-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6754f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6754f-115">-PassThru</span></span>
<span data-ttu-id="6754f-116">Retornará os detalhes do servidor excluídos se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="6754f-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6754f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6754f-117">-ResourceGroupName</span></span>
<span data-ttu-id="6754f-118">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="6754f-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6754f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6754f-119">-Confirm</span></span>
<span data-ttu-id="6754f-120">Solicita que o usuário confirme se deve executar a operação</span><span class="sxs-lookup"><span data-stu-id="6754f-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="6754f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6754f-121">-WhatIf</span></span>
<span data-ttu-id="6754f-122">Descreve as ações que a operação atual executará sem realmente performá-las</span><span class="sxs-lookup"><span data-stu-id="6754f-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="6754f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6754f-123">CommonParameters</span></span>
<span data-ttu-id="6754f-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6754f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6754f-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6754f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6754f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6754f-126">INPUTS</span></span>

### <span data-ttu-id="6754f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6754f-127">System.String</span></span>

## <span data-ttu-id="6754f-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6754f-128">OUTPUTS</span></span>

### <span data-ttu-id="6754f-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6754f-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="6754f-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="6754f-130">NOTES</span></span>
<span data-ttu-id="6754f-131">Alias: Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="6754f-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="6754f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6754f-132">RELATED LINKS</span></span>

[<span data-ttu-id="6754f-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6754f-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="6754f-134">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6754f-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)
