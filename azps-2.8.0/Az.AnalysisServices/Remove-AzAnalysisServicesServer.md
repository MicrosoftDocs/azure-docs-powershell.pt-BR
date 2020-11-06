---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: b64ba86a6aab80910ac09bd3757565df433690dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598159"
---
# <span data-ttu-id="2222d-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2222d-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="2222d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2222d-102">SYNOPSIS</span></span>
<span data-ttu-id="2222d-103">Exclui uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2222d-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="2222d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2222d-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2222d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2222d-105">DESCRIPTION</span></span>
<span data-ttu-id="2222d-106">O cmdlet Remove-AzAnalysisServicesServer exclui uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2222d-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="2222d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2222d-107">EXAMPLES</span></span>

### <span data-ttu-id="2222d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2222d-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="2222d-109">Esse comando removerá o servidor chamado TestServer do botão de teste do MySource</span><span class="sxs-lookup"><span data-stu-id="2222d-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="2222d-110">OS</span><span class="sxs-lookup"><span data-stu-id="2222d-110">PARAMETERS</span></span>

### <span data-ttu-id="2222d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2222d-111">-DefaultProfile</span></span>
<span data-ttu-id="2222d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2222d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2222d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2222d-113">-Name</span></span>
<span data-ttu-id="2222d-114">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2222d-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="2222d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2222d-115">-PassThru</span></span>
<span data-ttu-id="2222d-116">Retornará os detalhes do servidor excluído se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="2222d-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="2222d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2222d-117">-ResourceGroupName</span></span>
<span data-ttu-id="2222d-118">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="2222d-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="2222d-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2222d-119">-Confirm</span></span>
<span data-ttu-id="2222d-120">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="2222d-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2222d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2222d-121">-WhatIf</span></span>
<span data-ttu-id="2222d-122">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="2222d-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2222d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2222d-123">CommonParameters</span></span>
<span data-ttu-id="2222d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2222d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2222d-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2222d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2222d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2222d-126">INPUTS</span></span>

### <span data-ttu-id="2222d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2222d-127">System.String</span></span>

## <span data-ttu-id="2222d-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2222d-128">OUTPUTS</span></span>

### <span data-ttu-id="2222d-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2222d-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="2222d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2222d-130">NOTES</span></span>
<span data-ttu-id="2222d-131">Alias: Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="2222d-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="2222d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2222d-132">RELATED LINKS</span></span>

[<span data-ttu-id="2222d-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2222d-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="2222d-134">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2222d-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)
