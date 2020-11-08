---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: db35d5f6f0a8c8345fb10d13e4d2ca5c6169a090
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110623"
---
# <span data-ttu-id="deff3-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="deff3-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="deff3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="deff3-102">SYNOPSIS</span></span>
<span data-ttu-id="deff3-103">Cria uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="deff3-103">Creates a Batch account.</span></span>

## <span data-ttu-id="deff3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="deff3-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-PublicNetworkAccess <PublicNetworkAccessType>]
 [-IdentityType <ResourceIdentityType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deff3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="deff3-105">DESCRIPTION</span></span>
<span data-ttu-id="deff3-106">O cmdlet **New-AzBatchAccount** cria uma conta em lotes do Azure para o grupo de recursos e a localização especificados.</span><span class="sxs-lookup"><span data-stu-id="deff3-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="deff3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="deff3-107">EXAMPLES</span></span>

### <span data-ttu-id="deff3-108">Exemplo 1: criar uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="deff3-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="deff3-109">Esse comando cria uma conta em lotes chamada pfuller usando o grupo de recursos ResourceGroup03 no local do oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="deff3-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="deff3-110">OS</span><span class="sxs-lookup"><span data-stu-id="deff3-110">PARAMETERS</span></span>

### <span data-ttu-id="deff3-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="deff3-111">-AccountName</span></span>
<span data-ttu-id="deff3-112">Especifica o nome da conta em lotes que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="deff3-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="deff3-113">Os nomes de contas em lotes devem ter entre 3 e 24 caracteres de comprimento e conter apenas números e letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="deff3-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="deff3-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="deff3-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="deff3-115">Especifica a ID do recurso da conta de armazenamento a ser usada para armazenamento automático.</span><span class="sxs-lookup"><span data-stu-id="deff3-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="deff3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deff3-116">-DefaultProfile</span></span>
<span data-ttu-id="deff3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="deff3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deff3-118">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="deff3-118">-IdentityType</span></span>
<span data-ttu-id="deff3-119">A identidade associada ao BatchAccount</span><span class="sxs-lookup"><span data-stu-id="deff3-119">The identity associated with the BatchAccount</span></span>

```yaml
Type: Microsoft.Azure.Management.Batch.Models.ResourceIdentityType
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deff3-120">-Keyvaultid</span><span class="sxs-lookup"><span data-stu-id="deff3-120">-KeyVaultId</span></span>
<span data-ttu-id="deff3-121">A ID do recurso do cofre de chaves do Azure associado à conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="deff3-121">The resource ID of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="deff3-122">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="deff3-122">-KeyVaultUrl</span></span>
<span data-ttu-id="deff3-123">A URL do cofre de chaves do Azure associado à conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="deff3-123">The URL of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="deff3-124">-Local</span><span class="sxs-lookup"><span data-stu-id="deff3-124">-Location</span></span>
<span data-ttu-id="deff3-125">Especifica a região em que esse cmdlet cria a conta.</span><span class="sxs-lookup"><span data-stu-id="deff3-125">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="deff3-126">Para obter mais informações, consulte [regiões do Azure](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="deff3-126">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="deff3-127">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="deff3-127">-PoolAllocationMode</span></span>
<span data-ttu-id="deff3-128">O modo de alocação para a criação de grupos na conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="deff3-128">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deff3-129">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="deff3-129">-PublicNetworkAccess</span></span>
<span data-ttu-id="deff3-130">O tipo de acesso à rede pública</span><span class="sxs-lookup"><span data-stu-id="deff3-130">The public network access type</span></span>

```yaml
Type: Microsoft.Azure.Management.Batch.Models.PublicNetworkAccessType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deff3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deff3-131">-ResourceGroupName</span></span>
<span data-ttu-id="deff3-132">Especifica o nome do grupo de recursos no qual esse cmdlet cria a conta.</span><span class="sxs-lookup"><span data-stu-id="deff3-132">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="deff3-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="deff3-133">-Tag</span></span>
<span data-ttu-id="deff3-134">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="deff3-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="deff3-135">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="deff3-135">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="deff3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deff3-136">CommonParameters</span></span>
<span data-ttu-id="deff3-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deff3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deff3-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="deff3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deff3-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="deff3-139">INPUTS</span></span>

### <span data-ttu-id="deff3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="deff3-140">System.String</span></span>

### <span data-ttu-id="deff3-141">System. Nullable ' 1 [[Microsoft.Azure.Management.Batch. Models. PoolAllocationMode, Microsoft.Azure.Management.Batch, Version = 9.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="deff3-141">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=9.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="deff3-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="deff3-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="deff3-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="deff3-143">OUTPUTS</span></span>

### <span data-ttu-id="deff3-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="deff3-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="deff3-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="deff3-145">NOTES</span></span>

## <span data-ttu-id="deff3-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="deff3-146">RELATED LINKS</span></span>

[<span data-ttu-id="deff3-147">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="deff3-147">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="deff3-148">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="deff3-148">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="deff3-149">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="deff3-149">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="deff3-150">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="deff3-150">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
