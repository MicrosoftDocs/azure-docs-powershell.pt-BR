---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/remove-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 4976c34437b2f858f8e76924754fe04a8b1e0a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431482"
---
# <span data-ttu-id="40e96-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="40e96-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="40e96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40e96-102">SYNOPSIS</span></span>
<span data-ttu-id="40e96-103">Exclui uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="40e96-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40e96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40e96-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40e96-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40e96-105">DESCRIPTION</span></span>
<span data-ttu-id="40e96-106">O cmdlet Remove-AzureRmAnalysisServicesServer exclui uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="40e96-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="40e96-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40e96-107">EXAMPLES</span></span>

### <span data-ttu-id="40e96-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40e96-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="40e96-109">Esse comando removerá o servidor chamado TestServer do botão de teste do MySource</span><span class="sxs-lookup"><span data-stu-id="40e96-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="40e96-110">OS</span><span class="sxs-lookup"><span data-stu-id="40e96-110">PARAMETERS</span></span>

### <span data-ttu-id="40e96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e96-111">-DefaultProfile</span></span>
<span data-ttu-id="40e96-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40e96-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40e96-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="40e96-113">-Name</span></span>
<span data-ttu-id="40e96-114">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="40e96-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="40e96-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40e96-115">-PassThru</span></span>
<span data-ttu-id="40e96-116">Retornará os detalhes do servidor excluído se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="40e96-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="40e96-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e96-117">-ResourceGroupName</span></span>
<span data-ttu-id="40e96-118">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="40e96-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="40e96-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40e96-119">-Confirm</span></span>
<span data-ttu-id="40e96-120">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="40e96-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="40e96-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e96-121">-WhatIf</span></span>
<span data-ttu-id="40e96-122">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="40e96-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="40e96-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e96-123">CommonParameters</span></span>
<span data-ttu-id="40e96-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e96-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e96-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e96-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e96-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40e96-126">INPUTS</span></span>

### <span data-ttu-id="40e96-127">System. String</span><span class="sxs-lookup"><span data-stu-id="40e96-127">System.String</span></span>

## <span data-ttu-id="40e96-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40e96-128">OUTPUTS</span></span>

### <span data-ttu-id="40e96-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="40e96-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="40e96-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40e96-130">NOTES</span></span>
<span data-ttu-id="40e96-131">Alias: Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="40e96-131">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="40e96-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40e96-132">RELATED LINKS</span></span>

[<span data-ttu-id="40e96-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="40e96-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="40e96-134">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="40e96-134">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)