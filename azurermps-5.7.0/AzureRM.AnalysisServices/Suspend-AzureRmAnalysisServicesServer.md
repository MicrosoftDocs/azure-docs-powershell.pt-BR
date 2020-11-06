---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/suspend-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 116dfd9d38325682e6a80361b40bc8dd84b133fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428222"
---
# <span data-ttu-id="fb3c0-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="fb3c0-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="fb3c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb3c0-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3c0-103">Suspende uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="fb3c0-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb3c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb3c0-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb3c0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb3c0-105">DESCRIPTION</span></span>
<span data-ttu-id="fb3c0-106">O cmdlet Suspend-AzureRmAnalysisServicesServer suspende uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="fb3c0-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="fb3c0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb3c0-107">EXAMPLES</span></span>

### <span data-ttu-id="fb3c0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb3c0-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="fb3c0-109">Esse comando suspenderá um servidor ativo chamado TestServer no modo de teste do modo de Resource</span><span class="sxs-lookup"><span data-stu-id="fb3c0-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="fb3c0-110">OS</span><span class="sxs-lookup"><span data-stu-id="fb3c0-110">PARAMETERS</span></span>

### <span data-ttu-id="fb3c0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3c0-111">-DefaultProfile</span></span>
<span data-ttu-id="fb3c0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3c0-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb3c0-113">-Name</span></span>
<span data-ttu-id="fb3c0-114">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="fb3c0-114">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3c0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb3c0-115">-PassThru</span></span>
<span data-ttu-id="fb3c0-116">Retornará os detalhes do servidor excluído se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="fb3c0-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3c0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb3c0-117">-ResourceGroupName</span></span>
<span data-ttu-id="fb3c0-118">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="fb3c0-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3c0-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb3c0-119">-Confirm</span></span>
<span data-ttu-id="fb3c0-120">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="fb3c0-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3c0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3c0-121">-WhatIf</span></span>
<span data-ttu-id="fb3c0-122">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="fb3c0-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3c0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3c0-123">CommonParameters</span></span>
<span data-ttu-id="fb3c0-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3c0-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb3c0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3c0-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb3c0-126">INPUTS</span></span>

### <span data-ttu-id="fb3c0-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fb3c0-127">None</span></span>
<span data-ttu-id="fb3c0-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb3c0-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb3c0-129">OUTPUTS</span></span>

### <span data-ttu-id="fb3c0-130">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="fb3c0-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="fb3c0-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb3c0-131">NOTES</span></span>
<span data-ttu-id="fb3c0-132">Alias: Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="fb3c0-132">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="fb3c0-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb3c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="fb3c0-134">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="fb3c0-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="fb3c0-135">Currículo-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="fb3c0-135">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

