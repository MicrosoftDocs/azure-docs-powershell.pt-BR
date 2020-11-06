---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: fb55eec3dc0bf3cf83032251e017749a07970f2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427053"
---
# <span data-ttu-id="62239-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="62239-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="62239-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62239-102">SYNOPSIS</span></span>
<span data-ttu-id="62239-103">Exclui uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="62239-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62239-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62239-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62239-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62239-105">DESCRIPTION</span></span>
<span data-ttu-id="62239-106">O cmdlet Remove-AzureRmAnalysisServicesServer exclui uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="62239-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="62239-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62239-107">EXAMPLES</span></span>

### <span data-ttu-id="62239-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="62239-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="62239-109">Esse comando removerá o servidor chamado TestServer do botão de teste do MySource</span><span class="sxs-lookup"><span data-stu-id="62239-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="62239-110">OS</span><span class="sxs-lookup"><span data-stu-id="62239-110">PARAMETERS</span></span>

### <span data-ttu-id="62239-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="62239-111">-Name</span></span>
<span data-ttu-id="62239-112">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="62239-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="62239-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62239-113">-PassThru</span></span>
<span data-ttu-id="62239-114">Retornará os detalhes do servidor excluído se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="62239-114">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="62239-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62239-115">-ResourceGroupName</span></span>
<span data-ttu-id="62239-116">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="62239-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="62239-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="62239-117">-Confirm</span></span>
<span data-ttu-id="62239-118">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="62239-118">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="62239-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62239-119">-WhatIf</span></span>
<span data-ttu-id="62239-120">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="62239-120">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="62239-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62239-121">-DefaultProfile</span></span>
<span data-ttu-id="62239-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62239-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62239-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62239-123">CommonParameters</span></span>
<span data-ttu-id="62239-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62239-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62239-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62239-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62239-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62239-126">INPUTS</span></span>

## <span data-ttu-id="62239-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62239-127">OUTPUTS</span></span>

### <span data-ttu-id="62239-128">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="62239-128">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="62239-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62239-129">NOTES</span></span>
<span data-ttu-id="62239-130">Alias: Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="62239-130">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="62239-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62239-131">RELATED LINKS</span></span>

[<span data-ttu-id="62239-132">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="62239-132">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="62239-133">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="62239-133">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)
