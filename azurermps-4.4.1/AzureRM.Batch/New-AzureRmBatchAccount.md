---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: ed44fa5960935bbe353d775a426e023512327e7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602771"
---
# <span data-ttu-id="59a5a-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="59a5a-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="59a5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="59a5a-103">Cria uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="59a5a-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59a5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59a5a-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59a5a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="59a5a-106">O cmdlet **New-AzureRmBatchAccount** cria uma conta em lotes do Azure para o grupo de recursos e a localização especificados.</span><span class="sxs-lookup"><span data-stu-id="59a5a-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="59a5a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59a5a-107">EXAMPLES</span></span>

### <span data-ttu-id="59a5a-108">Exemplo 1: criar uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="59a5a-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="59a5a-109">Esse comando cria uma conta em lotes chamada pfuller usando o grupo de recursos ResourceGroup03 no local do oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="59a5a-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="59a5a-110">OS</span><span class="sxs-lookup"><span data-stu-id="59a5a-110">PARAMETERS</span></span>

### <span data-ttu-id="59a5a-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="59a5a-111">-AccountName</span></span>
<span data-ttu-id="59a5a-112">Especifica o nome da conta em lotes que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="59a5a-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="59a5a-113">Os nomes de contas em lotes devem ter entre 3 e 24 caracteres de comprimento e conter apenas números e letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="59a5a-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="59a5a-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="59a5a-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="59a5a-115">Especifica a ID do recurso da conta de armazenamento a ser usada para armazenamento automático.</span><span class="sxs-lookup"><span data-stu-id="59a5a-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59a5a-116">-Local</span><span class="sxs-lookup"><span data-stu-id="59a5a-116">-Location</span></span>
<span data-ttu-id="59a5a-117">Especifica a região em que esse cmdlet cria a conta.</span><span class="sxs-lookup"><span data-stu-id="59a5a-117">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="59a5a-118">Para obter mais informações, consulte [regiões do Azure](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="59a5a-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="59a5a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a5a-119">-ResourceGroupName</span></span>
<span data-ttu-id="59a5a-120">Especifica o nome do grupo de recursos no qual esse cmdlet cria a conta.</span><span class="sxs-lookup"><span data-stu-id="59a5a-120">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59a5a-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="59a5a-121">-Tag</span></span>
<span data-ttu-id="59a5a-122">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="59a5a-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="59a5a-123">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="59a5a-123">For example:</span></span>

<span data-ttu-id="59a5a-124">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="59a5a-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59a5a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a5a-125">-DefaultProfile</span></span>
<span data-ttu-id="59a5a-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59a5a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59a5a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a5a-127">CommonParameters</span></span>
<span data-ttu-id="59a5a-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a5a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a5a-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59a5a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a5a-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59a5a-130">INPUTS</span></span>

## <span data-ttu-id="59a5a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59a5a-131">OUTPUTS</span></span>

### <span data-ttu-id="59a5a-132">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="59a5a-132">BatchAccountContext</span></span>

## <span data-ttu-id="59a5a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59a5a-133">NOTES</span></span>

## <span data-ttu-id="59a5a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59a5a-134">RELATED LINKS</span></span>

[<span data-ttu-id="59a5a-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="59a5a-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="59a5a-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="59a5a-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="59a5a-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="59a5a-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="59a5a-138">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="59a5a-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
