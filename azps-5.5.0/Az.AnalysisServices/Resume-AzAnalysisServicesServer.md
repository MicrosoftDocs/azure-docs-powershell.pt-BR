---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 3614c62af825b109b224d231d89dda315a7e2616
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114861"
---
# <span data-ttu-id="f8d19-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f8d19-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="f8d19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8d19-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d19-103">Retoma uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f8d19-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="f8d19-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8d19-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8d19-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8d19-105">DESCRIPTION</span></span>
<span data-ttu-id="f8d19-106">O Resume-AzAnalysisServicesServer cmdlet retoma uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f8d19-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="f8d19-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f8d19-107">EXAMPLES</span></span>

### <span data-ttu-id="f8d19-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f8d19-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="f8d19-109">Esse comando retomará um servidor pausado chamado testserver no grupo de teste de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f8d19-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="f8d19-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8d19-110">PARAMETERS</span></span>

### <span data-ttu-id="f8d19-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d19-111">-DefaultProfile</span></span>
<span data-ttu-id="f8d19-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f8d19-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8d19-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8d19-113">-Name</span></span>
<span data-ttu-id="f8d19-114">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f8d19-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="f8d19-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8d19-115">-PassThru</span></span>
<span data-ttu-id="f8d19-116">Retornará os detalhes do servidor excluídos se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="f8d19-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="f8d19-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8d19-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8d19-118">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="f8d19-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="f8d19-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f8d19-119">-Confirm</span></span>
<span data-ttu-id="f8d19-120">Solicita que o usuário confirme se a operação será realizada</span><span class="sxs-lookup"><span data-stu-id="f8d19-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="f8d19-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d19-121">-WhatIf</span></span>
<span data-ttu-id="f8d19-122">Descreve as ações que a operação atual executará sem realmente executa-las</span><span class="sxs-lookup"><span data-stu-id="f8d19-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="f8d19-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d19-123">CommonParameters</span></span>
<span data-ttu-id="f8d19-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8d19-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d19-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8d19-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d19-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="f8d19-126">INPUTS</span></span>

### <span data-ttu-id="f8d19-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f8d19-127">System.String</span></span>

## <span data-ttu-id="f8d19-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="f8d19-128">OUTPUTS</span></span>

### <span data-ttu-id="f8d19-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f8d19-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="f8d19-130">Notas</span><span class="sxs-lookup"><span data-stu-id="f8d19-130">NOTES</span></span>
<span data-ttu-id="f8d19-131">Alias: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="f8d19-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="f8d19-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8d19-132">RELATED LINKS</span></span>

[<span data-ttu-id="f8d19-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f8d19-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="f8d19-134">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f8d19-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
