---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 44627bd5ffa7340a10866605598d981b10f35a58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125051"
---
# <span data-ttu-id="8be74-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8be74-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="8be74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8be74-102">SYNOPSIS</span></span>
<span data-ttu-id="8be74-103">Atualiza uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="8be74-103">Updates a Batch account.</span></span>

## <span data-ttu-id="8be74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8be74-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8be74-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8be74-105">DESCRIPTION</span></span>
<span data-ttu-id="8be74-106">O cmdlet **set-AzBatchAccount** atualiza uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="8be74-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="8be74-107">Atualmente, esse cmdlet pode atualizar apenas as marcas.</span><span class="sxs-lookup"><span data-stu-id="8be74-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="8be74-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8be74-108">EXAMPLES</span></span>

### <span data-ttu-id="8be74-109">Exemplo 1: atualizar as marcas em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="8be74-109">Example 1: Update the tags on a Batch account</span></span>
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

<span data-ttu-id="8be74-110">Esse comando atualiza as marcas na conta chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="8be74-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="8be74-111">OS</span><span class="sxs-lookup"><span data-stu-id="8be74-111">PARAMETERS</span></span>

### <span data-ttu-id="8be74-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8be74-112">-AccountName</span></span>
<span data-ttu-id="8be74-113">Especifica o nome da conta em lotes que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="8be74-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="8be74-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8be74-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="8be74-115">Especifica a ID do recurso da conta de armazenamento a ser usada para armazenamento automático.</span><span class="sxs-lookup"><span data-stu-id="8be74-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="8be74-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be74-116">-DefaultProfile</span></span>
<span data-ttu-id="8be74-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8be74-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8be74-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be74-118">-ResourceGroupName</span></span>
<span data-ttu-id="8be74-119">Especifica o grupo de recursos da conta em que este cmdlet é atualizado.</span><span class="sxs-lookup"><span data-stu-id="8be74-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="8be74-120">-Marca</span><span class="sxs-lookup"><span data-stu-id="8be74-120">-Tag</span></span>
<span data-ttu-id="8be74-121">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8be74-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8be74-122">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8be74-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8be74-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be74-123">CommonParameters</span></span>
<span data-ttu-id="8be74-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be74-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be74-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8be74-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be74-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8be74-126">INPUTS</span></span>

### <span data-ttu-id="8be74-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8be74-127">System.String</span></span>

### <span data-ttu-id="8be74-128">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8be74-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8be74-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8be74-129">OUTPUTS</span></span>

### <span data-ttu-id="8be74-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8be74-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8be74-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8be74-131">NOTES</span></span>

## <span data-ttu-id="8be74-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8be74-132">RELATED LINKS</span></span>

[<span data-ttu-id="8be74-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8be74-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="8be74-134">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8be74-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="8be74-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8be74-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="8be74-136">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="8be74-136">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
