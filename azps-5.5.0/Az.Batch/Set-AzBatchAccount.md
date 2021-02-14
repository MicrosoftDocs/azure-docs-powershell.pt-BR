---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 44627bd5ffa7340a10866605598d981b10f35a58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116959"
---
# <span data-ttu-id="3186d-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3186d-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="3186d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3186d-102">SYNOPSIS</span></span>
<span data-ttu-id="3186d-103">Atualiza uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="3186d-103">Updates a Batch account.</span></span>

## <span data-ttu-id="3186d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3186d-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3186d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3186d-105">DESCRIPTION</span></span>
<span data-ttu-id="3186d-106">O **cmdlet Set-AzBatchAccount** atualiza uma conta do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="3186d-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="3186d-107">Atualmente, esse cmdlet pode atualizar apenas marcas.</span><span class="sxs-lookup"><span data-stu-id="3186d-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="3186d-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3186d-108">EXAMPLES</span></span>

### <span data-ttu-id="3186d-109">Exemplo 1: Atualizar as marcas em uma conta em lote</span><span class="sxs-lookup"><span data-stu-id="3186d-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="3186d-110">Este comando atualiza as marcas na conta chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="3186d-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="3186d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3186d-111">PARAMETERS</span></span>

### <span data-ttu-id="3186d-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="3186d-112">-AccountName</span></span>
<span data-ttu-id="3186d-113">Especifica o nome da conta Em lotes que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="3186d-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186d-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3186d-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="3186d-115">Especifica a ID de recurso da conta de armazenamento a ser usada para o armazenamento automático.</span><span class="sxs-lookup"><span data-stu-id="3186d-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="3186d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3186d-116">-DefaultProfile</span></span>
<span data-ttu-id="3186d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3186d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3186d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3186d-118">-ResourceGroupName</span></span>
<span data-ttu-id="3186d-119">Especifica o grupo de recursos da conta que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="3186d-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="3186d-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="3186d-120">-Tag</span></span>
<span data-ttu-id="3186d-121">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="3186d-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3186d-122">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="3186d-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3186d-123">CommonParameters</span></span>
<span data-ttu-id="3186d-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3186d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3186d-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3186d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3186d-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="3186d-126">INPUTS</span></span>

### <span data-ttu-id="3186d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="3186d-127">System.String</span></span>

### <span data-ttu-id="3186d-128">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3186d-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3186d-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="3186d-129">OUTPUTS</span></span>

### <span data-ttu-id="3186d-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3186d-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3186d-131">Notas</span><span class="sxs-lookup"><span data-stu-id="3186d-131">NOTES</span></span>

## <span data-ttu-id="3186d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3186d-132">RELATED LINKS</span></span>

[<span data-ttu-id="3186d-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3186d-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="3186d-134">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3186d-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="3186d-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3186d-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="3186d-136">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="3186d-136">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
