---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
ms.openlocfilehash: 7f1747d838d0b81d1cfa29e98134897357f33a53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427683"
---
# <span data-ttu-id="25412-101">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="25412-101">Set-AzureRmBatchAccount</span></span>

## <span data-ttu-id="25412-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25412-102">SYNOPSIS</span></span>
<span data-ttu-id="25412-103">Atualiza uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="25412-103">Updates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25412-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25412-104">SYNTAX</span></span>

```
Set-AzureRmBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25412-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25412-105">DESCRIPTION</span></span>
<span data-ttu-id="25412-106">O cmdlet **set-AzureRmBatchAccount** atualiza uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="25412-106">The **Set-AzureRmBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="25412-107">Atualmente, esse cmdlet pode atualizar apenas as marcas.</span><span class="sxs-lookup"><span data-stu-id="25412-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="25412-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25412-108">EXAMPLES</span></span>

### <span data-ttu-id="25412-109">Exemplo 1: atualizar as marcas em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="25412-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
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

<span data-ttu-id="25412-110">Esse comando atualiza as marcas na conta chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="25412-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="25412-111">OS</span><span class="sxs-lookup"><span data-stu-id="25412-111">PARAMETERS</span></span>

### <span data-ttu-id="25412-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="25412-112">-AccountName</span></span>
<span data-ttu-id="25412-113">Especifica o nome da conta em lotes que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="25412-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25412-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="25412-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="25412-115">Especifica a ID do recurso da conta de armazenamento a ser usada para armazenamento automático.</span><span class="sxs-lookup"><span data-stu-id="25412-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25412-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25412-116">-DefaultProfile</span></span>
<span data-ttu-id="25412-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25412-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25412-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25412-118">-ResourceGroupName</span></span>
<span data-ttu-id="25412-119">Especifica o grupo de recursos da conta em que este cmdlet é atualizado.</span><span class="sxs-lookup"><span data-stu-id="25412-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25412-120">-Marca</span><span class="sxs-lookup"><span data-stu-id="25412-120">-Tag</span></span>
<span data-ttu-id="25412-121">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="25412-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="25412-122">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="25412-122">For example:</span></span>

<span data-ttu-id="25412-123">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="25412-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25412-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25412-124">CommonParameters</span></span>
<span data-ttu-id="25412-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25412-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25412-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25412-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25412-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25412-127">INPUTS</span></span>

### <span data-ttu-id="25412-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="25412-128">None</span></span>
<span data-ttu-id="25412-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="25412-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25412-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25412-130">OUTPUTS</span></span>

### <span data-ttu-id="25412-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="25412-131">BatchAccountContext</span></span>

## <span data-ttu-id="25412-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25412-132">NOTES</span></span>

## <span data-ttu-id="25412-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25412-133">RELATED LINKS</span></span>

[<span data-ttu-id="25412-134">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="25412-134">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="25412-135">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="25412-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="25412-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="25412-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="25412-137">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="25412-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
