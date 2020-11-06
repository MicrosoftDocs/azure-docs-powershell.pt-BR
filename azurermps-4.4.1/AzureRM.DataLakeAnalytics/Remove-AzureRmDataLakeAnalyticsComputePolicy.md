---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 8be60712f0687edcbd036c48a079e3ecb90ec6c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433156"
---
# <span data-ttu-id="00c84-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="00c84-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="00c84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00c84-102">SYNOPSIS</span></span>
<span data-ttu-id="00c84-103">Remove uma política de computação do Azure data Lake Analytics especificada</span><span class="sxs-lookup"><span data-stu-id="00c84-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00c84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00c84-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00c84-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00c84-105">DESCRIPTION</span></span>
<span data-ttu-id="00c84-106">Remove **-AzureRmDataLakeAnalyticsComputePolicy** remove uma política de computação do Azure data Lake Analytics especificada.</span><span class="sxs-lookup"><span data-stu-id="00c84-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="00c84-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00c84-107">EXAMPLES</span></span>

### <span data-ttu-id="00c84-108">Exemplo 1: remover uma política de computação</span><span class="sxs-lookup"><span data-stu-id="00c84-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="00c84-109">Este comando Remove a política de computação especificada com o nome ' MyPolicy ' na conta ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="00c84-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="00c84-110">OS</span><span class="sxs-lookup"><span data-stu-id="00c84-110">PARAMETERS</span></span>

### <span data-ttu-id="00c84-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="00c84-111">-Account</span></span>
<span data-ttu-id="00c84-112">Nome da conta da qual remover a política de computação.</span><span class="sxs-lookup"><span data-stu-id="00c84-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="00c84-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="00c84-113">-Name</span></span>
<span data-ttu-id="00c84-114">Nome da política de computação a ser removida.</span><span class="sxs-lookup"><span data-stu-id="00c84-114">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="00c84-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00c84-115">-PassThru</span></span>
<span data-ttu-id="00c84-116">Retornar true após a exclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="00c84-116">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="00c84-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00c84-117">-ResourceGroupName</span></span>
<span data-ttu-id="00c84-118">Nome do grupo de recursos sob o qual a conta existe.</span><span class="sxs-lookup"><span data-stu-id="00c84-118">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="00c84-119">Opcional e tentará descobrir, se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="00c84-119">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="00c84-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="00c84-120">-Confirm</span></span>
<span data-ttu-id="00c84-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00c84-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00c84-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00c84-122">-WhatIf</span></span>
<span data-ttu-id="00c84-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00c84-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00c84-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00c84-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00c84-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00c84-125">-DefaultProfile</span></span>
<span data-ttu-id="00c84-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00c84-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00c84-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c84-127">CommonParameters</span></span>
<span data-ttu-id="00c84-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00c84-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c84-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00c84-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c84-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00c84-130">INPUTS</span></span>

### <span data-ttu-id="00c84-131">System. String</span><span class="sxs-lookup"><span data-stu-id="00c84-131">System.String</span></span>

## <span data-ttu-id="00c84-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00c84-132">OUTPUTS</span></span>

### <span data-ttu-id="00c84-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="00c84-133">System.Boolean</span></span>

## <span data-ttu-id="00c84-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00c84-134">NOTES</span></span>

## <span data-ttu-id="00c84-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00c84-135">RELATED LINKS</span></span>

