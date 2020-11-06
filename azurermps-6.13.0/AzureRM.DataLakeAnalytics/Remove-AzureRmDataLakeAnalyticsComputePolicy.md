---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: a97c6835144cda227fc07645f087e393cda2b8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428497"
---
# <span data-ttu-id="a1c5e-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="a1c5e-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="a1c5e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c5e-103">Remove uma política de computação do Azure data Lake Analytics especificada</span><span class="sxs-lookup"><span data-stu-id="a1c5e-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1c5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1c5e-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1c5e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1c5e-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c5e-106">Remove **-AzureRmDataLakeAnalyticsComputePolicy** remove uma política de computação do Azure data Lake Analytics especificada.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="a1c5e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1c5e-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c5e-108">Exemplo 1: remover uma política de computação</span><span class="sxs-lookup"><span data-stu-id="a1c5e-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="a1c5e-109">Este comando Remove a política de computação especificada com o nome ' MyPolicy ' na conta ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="a1c5e-110">OS</span><span class="sxs-lookup"><span data-stu-id="a1c5e-110">PARAMETERS</span></span>

### <span data-ttu-id="a1c5e-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="a1c5e-111">-Account</span></span>
<span data-ttu-id="a1c5e-112">Nome da conta da qual remover a política de computação.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="a1c5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c5e-113">-DefaultProfile</span></span>
<span data-ttu-id="a1c5e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a1c5e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1c5e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1c5e-115">-Name</span></span>
<span data-ttu-id="a1c5e-116">Nome da política de computação a ser removida.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="a1c5e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1c5e-117">-PassThru</span></span>
<span data-ttu-id="a1c5e-118">Retornar true após a exclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="a1c5e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c5e-119">-ResourceGroupName</span></span>
<span data-ttu-id="a1c5e-120">Nome do grupo de recursos sob o qual a conta existe.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="a1c5e-121">Opcional e tentará descobrir, se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="a1c5e-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1c5e-122">-Confirm</span></span>
<span data-ttu-id="a1c5e-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1c5e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1c5e-124">-WhatIf</span></span>
<span data-ttu-id="a1c5e-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1c5e-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1c5e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c5e-127">CommonParameters</span></span>
<span data-ttu-id="a1c5e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c5e-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c5e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c5e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1c5e-130">INPUTS</span></span>

### <span data-ttu-id="a1c5e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a1c5e-131">System.String</span></span>

## <span data-ttu-id="a1c5e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1c5e-132">OUTPUTS</span></span>

### <span data-ttu-id="a1c5e-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1c5e-133">System.Boolean</span></span>

## <span data-ttu-id="a1c5e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1c5e-134">NOTES</span></span>

## <span data-ttu-id="a1c5e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1c5e-135">RELATED LINKS</span></span>
