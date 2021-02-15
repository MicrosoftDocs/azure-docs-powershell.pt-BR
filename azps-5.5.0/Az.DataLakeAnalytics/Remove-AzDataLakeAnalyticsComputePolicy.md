---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115415"
---
# <span data-ttu-id="15b6f-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="15b6f-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="15b6f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="15b6f-103">Remove uma política de computação especificada do Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="15b6f-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="15b6f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15b6f-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15b6f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="15b6f-105">DESCRIPTION</span></span>
<span data-ttu-id="15b6f-106">O **Remove-AzDataLakeAnalyticsComputePolicy** remove uma política de computação especificada do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="15b6f-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="15b6f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="15b6f-107">EXAMPLES</span></span>

### <span data-ttu-id="15b6f-108">Exemplo 1: Remover uma política de computação</span><span class="sxs-lookup"><span data-stu-id="15b6f-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="15b6f-109">Esse comando remove a política de computação especificada com o nome 'myPolicy' na conta 'contosoadla'.</span><span class="sxs-lookup"><span data-stu-id="15b6f-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="15b6f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15b6f-110">PARAMETERS</span></span>

### <span data-ttu-id="15b6f-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="15b6f-111">-Account</span></span>
<span data-ttu-id="15b6f-112">Nome da conta para remover a política de computação.</span><span class="sxs-lookup"><span data-stu-id="15b6f-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="15b6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b6f-113">-DefaultProfile</span></span>
<span data-ttu-id="15b6f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="15b6f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15b6f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="15b6f-115">-Name</span></span>
<span data-ttu-id="15b6f-116">Nome da política de computação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="15b6f-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="15b6f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15b6f-117">-PassThru</span></span>
<span data-ttu-id="15b6f-118">Retornar verdadeiro após a exclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="15b6f-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="15b6f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15b6f-119">-ResourceGroupName</span></span>
<span data-ttu-id="15b6f-120">Nome do grupo de recursos no qual a conta existe.</span><span class="sxs-lookup"><span data-stu-id="15b6f-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="15b6f-121">Opcional e tentará descobrir se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="15b6f-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="15b6f-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="15b6f-122">-Confirm</span></span>
<span data-ttu-id="15b6f-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15b6f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15b6f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15b6f-124">-WhatIf</span></span>
<span data-ttu-id="15b6f-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="15b6f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15b6f-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15b6f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15b6f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b6f-127">CommonParameters</span></span>
<span data-ttu-id="15b6f-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b6f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b6f-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b6f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b6f-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="15b6f-130">INPUTS</span></span>

### <span data-ttu-id="15b6f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="15b6f-131">System.String</span></span>

## <span data-ttu-id="15b6f-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="15b6f-132">OUTPUTS</span></span>

### <span data-ttu-id="15b6f-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="15b6f-133">System.Boolean</span></span>

## <span data-ttu-id="15b6f-134">Notas</span><span class="sxs-lookup"><span data-stu-id="15b6f-134">NOTES</span></span>

## <span data-ttu-id="15b6f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15b6f-135">RELATED LINKS</span></span>
