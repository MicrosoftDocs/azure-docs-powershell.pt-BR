---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 3f7ed1a36cc95296ee7fdeec45c5039063032d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427819"
---
# <span data-ttu-id="a837e-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a837e-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="a837e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a837e-102">SYNOPSIS</span></span>
<span data-ttu-id="a837e-103">Remove um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a837e-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a837e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a837e-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a837e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a837e-105">DESCRIPTION</span></span>
<span data-ttu-id="a837e-106">O cmdlet **Remove-AzureRmOperationalInsightsWorkspace** exclui um espaço de trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="a837e-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="a837e-107">Se esse espaço de trabalho tiver sido vinculado a uma conta existente por meio do parâmetro *CódigoDoCliente* no momento da criação, a conta original não será excluída no portal dos insights operacionais.</span><span class="sxs-lookup"><span data-stu-id="a837e-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="a837e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a837e-108">EXAMPLES</span></span>

### <span data-ttu-id="a837e-109">Exemplo 1: remover um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="a837e-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="a837e-110">Esse comando Remove o espaço de trabalho chamado MyWorkspace do grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a837e-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="a837e-111">Exemplo 2: remover um espaço de trabalho usando o pipeline e sem confirmação</span><span class="sxs-lookup"><span data-stu-id="a837e-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="a837e-112">Esse comando usa o cmdlet Get-AzureRmOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, o passa para o cmdlet **Remove-AzureRmOperationalInsightsWorkspace** usando o operador pipeline para removê-lo.</span><span class="sxs-lookup"><span data-stu-id="a837e-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="a837e-113">Como o parâmetro *Force* é especificado, o comando não o avisa antes de remover o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a837e-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="a837e-114">OS</span><span class="sxs-lookup"><span data-stu-id="a837e-114">PARAMETERS</span></span>

### <span data-ttu-id="a837e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a837e-115">-Force</span></span>
<span data-ttu-id="a837e-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a837e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a837e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a837e-117">-Name</span></span>
<span data-ttu-id="a837e-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a837e-118">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a837e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a837e-119">-ResourceGroupName</span></span>
<span data-ttu-id="a837e-120">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a837e-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="a837e-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a837e-121">-Confirm</span></span>
<span data-ttu-id="a837e-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a837e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a837e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a837e-123">-WhatIf</span></span>
<span data-ttu-id="a837e-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a837e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a837e-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a837e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a837e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a837e-126">-DefaultProfile</span></span>
<span data-ttu-id="a837e-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a837e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a837e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a837e-128">CommonParameters</span></span>
<span data-ttu-id="a837e-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a837e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a837e-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a837e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a837e-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a837e-131">INPUTS</span></span>

## <span data-ttu-id="a837e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a837e-132">OUTPUTS</span></span>

## <span data-ttu-id="a837e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a837e-133">NOTES</span></span>

## <span data-ttu-id="a837e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a837e-134">RELATED LINKS</span></span>

[<span data-ttu-id="a837e-135">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="a837e-135">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="a837e-136">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a837e-136">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


