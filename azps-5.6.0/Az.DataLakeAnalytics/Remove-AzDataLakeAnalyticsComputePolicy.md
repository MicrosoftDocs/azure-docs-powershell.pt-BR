---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1e6f6957adc8a67e1d92c0aad6f2be035b4f390d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886776"
---
# <span data-ttu-id="76f2c-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="76f2c-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="76f2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="76f2c-103">Remove uma política de computação do Azure Data Lake Analytics especificada</span><span class="sxs-lookup"><span data-stu-id="76f2c-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="76f2c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="76f2c-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76f2c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="76f2c-105">DESCRIPTION</span></span>
<span data-ttu-id="76f2c-106">A política de computação **Remove-AzDataLakeAnalyticsComputePolicy** remove uma política de computação do Azure Data Lake Analytics especificada.</span><span class="sxs-lookup"><span data-stu-id="76f2c-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="76f2c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76f2c-107">EXAMPLES</span></span>

### <span data-ttu-id="76f2c-108">Exemplo 1: Remover uma política de computação</span><span class="sxs-lookup"><span data-stu-id="76f2c-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="76f2c-109">Este comando remove a política de computação especificada com o nome 'myPolicy' na conta 'contosoadla'.</span><span class="sxs-lookup"><span data-stu-id="76f2c-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="76f2c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="76f2c-110">PARAMETERS</span></span>

### <span data-ttu-id="76f2c-111">-Account</span><span class="sxs-lookup"><span data-stu-id="76f2c-111">-Account</span></span>
<span data-ttu-id="76f2c-112">Nome da conta para remover a política de computação.</span><span class="sxs-lookup"><span data-stu-id="76f2c-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f2c-113">-DefaultProfile</span></span>
<span data-ttu-id="76f2c-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="76f2c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76f2c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="76f2c-115">-Name</span></span>
<span data-ttu-id="76f2c-116">Nome da política de computação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="76f2c-116">Name of the compute policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f2c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76f2c-117">-PassThru</span></span>
<span data-ttu-id="76f2c-118">Retornar true após a exclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="76f2c-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="76f2c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f2c-119">-ResourceGroupName</span></span>
<span data-ttu-id="76f2c-120">Nome do grupo de recursos no qual você a conta existe.</span><span class="sxs-lookup"><span data-stu-id="76f2c-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="76f2c-121">Opcional e tentará descobrir se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="76f2c-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f2c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76f2c-122">-Confirm</span></span>
<span data-ttu-id="76f2c-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f2c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76f2c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76f2c-124">-WhatIf</span></span>
<span data-ttu-id="76f2c-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76f2c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76f2c-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76f2c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76f2c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f2c-127">CommonParameters</span></span>
<span data-ttu-id="76f2c-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f2c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f2c-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76f2c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f2c-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76f2c-130">INPUTS</span></span>

### <span data-ttu-id="76f2c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="76f2c-131">System.String</span></span>

## <span data-ttu-id="76f2c-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="76f2c-132">OUTPUTS</span></span>

### <span data-ttu-id="76f2c-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76f2c-133">System.Boolean</span></span>

## <span data-ttu-id="76f2c-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="76f2c-134">NOTES</span></span>

## <span data-ttu-id="76f2c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76f2c-135">RELATED LINKS</span></span>
