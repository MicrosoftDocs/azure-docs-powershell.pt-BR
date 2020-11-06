---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 48080fde4c7187bcbcf601cb136373cc16ef7503
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93601898"
---
# <span data-ttu-id="b7710-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b7710-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="b7710-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7710-102">SYNOPSIS</span></span>
<span data-ttu-id="b7710-103">Obtém uma conta em lotes na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b7710-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="b7710-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7710-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7710-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7710-105">DESCRIPTION</span></span>
<span data-ttu-id="b7710-106">O cmdlet **Get-AzBatchAccount** Obtém uma conta em lotes do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b7710-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="b7710-107">Você pode usar o parâmetro *AccountName* para obter uma única conta ou pode usar o parâmetro *ResourceGroupName* para obter contas sob esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7710-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="b7710-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7710-108">EXAMPLES</span></span>

### <span data-ttu-id="b7710-109">Exemplo 1: obter uma conta em lotes por nome</span><span class="sxs-lookup"><span data-stu-id="b7710-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="b7710-110">Esse comando obtém a conta em lotes chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="b7710-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="b7710-111">Exemplo 2: obter as contas em lotes associadas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b7710-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="b7710-112">Esse comando obtém as contas em lotes associadas ao grupo de recursos CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="b7710-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="b7710-113">OS</span><span class="sxs-lookup"><span data-stu-id="b7710-113">PARAMETERS</span></span>

### <span data-ttu-id="b7710-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b7710-114">-AccountName</span></span>
<span data-ttu-id="b7710-115">Especifica o nome de uma conta.</span><span class="sxs-lookup"><span data-stu-id="b7710-115">Specifies the name of an account.</span></span>
<span data-ttu-id="b7710-116">Se você especificar um nome de conta, esse cmdlet retornará apenas essa conta.</span><span class="sxs-lookup"><span data-stu-id="b7710-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7710-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7710-117">-DefaultProfile</span></span>
<span data-ttu-id="b7710-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7710-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7710-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7710-119">-ResourceGroupName</span></span>
<span data-ttu-id="b7710-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7710-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b7710-121">Se você especificar um grupo de recursos, esse cmdlet obterá as contas sob o grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b7710-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

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

### <span data-ttu-id="b7710-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="b7710-122">-Tag</span></span>
<span data-ttu-id="b7710-123">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b7710-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b7710-124">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"} esse cmdlet obtém contas que contêm as marcas que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b7710-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7710-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7710-125">CommonParameters</span></span>
<span data-ttu-id="b7710-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7710-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7710-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7710-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7710-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7710-128">INPUTS</span></span>

### <span data-ttu-id="b7710-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b7710-129">System.String</span></span>

### <span data-ttu-id="b7710-130">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b7710-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b7710-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7710-131">OUTPUTS</span></span>

### <span data-ttu-id="b7710-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b7710-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b7710-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7710-133">NOTES</span></span>

## <span data-ttu-id="b7710-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7710-134">RELATED LINKS</span></span>

[<span data-ttu-id="b7710-135">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b7710-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="b7710-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b7710-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="b7710-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b7710-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="b7710-138">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="b7710-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
