---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6289aa916b4d03559fccb11ea0a8897f4b506b53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431153"
---
# <span data-ttu-id="f21c4-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="f21c4-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="f21c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f21c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f21c4-103">Cria uma conta de usuário em um nó de computação em lotes.</span><span class="sxs-lookup"><span data-stu-id="f21c4-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f21c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f21c4-104">SYNTAX</span></span>

### <span data-ttu-id="f21c4-105">%</span><span class="sxs-lookup"><span data-stu-id="f21c4-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f21c4-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="f21c4-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f21c4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f21c4-107">DESCRIPTION</span></span>
<span data-ttu-id="f21c4-108">O cmdlet **New-AzureBatchComputeNodeUser** cria uma conta de usuário em um nó de computação em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="f21c4-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="f21c4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f21c4-109">EXAMPLES</span></span>

### <span data-ttu-id="f21c4-110">Exemplo 1: criar uma conta de usuário que tenha credenciais administrativas</span><span class="sxs-lookup"><span data-stu-id="f21c4-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="f21c4-111">Esse comando cria uma conta de usuário no nó de computação que tem a ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="f21c4-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="f21c4-112">O nó está no pool que tem a ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="f21c4-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="f21c4-113">O nome de usuário é testuser, a senha é password, a conta expira em sete dias e a conta tem credenciais administrativas.</span><span class="sxs-lookup"><span data-stu-id="f21c4-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="f21c4-114">Exemplo 2: criar uma conta de usuário em um nó de computação usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="f21c4-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="f21c4-115">Esse comando obtém o nó de computação chamado ComputeNode01 usando o cmdlet **Get-AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="f21c4-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="f21c4-116">Esse nó está no pool que tem a ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="f21c4-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="f21c4-117">O comando passa aquele nó COMPUTE para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="f21c4-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f21c4-118">O comando cria uma conta de usuário com o nome de usuário TestUserand a senha.</span><span class="sxs-lookup"><span data-stu-id="f21c4-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="f21c4-119">OS</span><span class="sxs-lookup"><span data-stu-id="f21c4-119">PARAMETERS</span></span>

### <span data-ttu-id="f21c4-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f21c4-120">-BatchContext</span></span>
<span data-ttu-id="f21c4-121">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="f21c4-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f21c4-122">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="f21c4-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="f21c4-123">-ComputeNode</span></span>
<span data-ttu-id="f21c4-124">Especifica o nó de computação, como um objeto **PSComputeNode** , em que esse cmdlet cria uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="f21c4-124">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-125">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="f21c4-125">-ComputeNodeId</span></span>
<span data-ttu-id="f21c4-126">Especifica a ID do nó de computação em que esse cmdlet cria uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="f21c4-126">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f21c4-127">-ExpiryTime</span></span>
<span data-ttu-id="f21c4-128">Especifica o tempo de expiração da nova conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="f21c4-128">Specifies the expiry time for the new user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-129">-ISAdmin</span><span class="sxs-lookup"><span data-stu-id="f21c4-129">-IsAdmin</span></span>
<span data-ttu-id="f21c4-130">Indica que o cmdlet cria uma conta de usuário que tem credenciais administrativas.</span><span class="sxs-lookup"><span data-stu-id="f21c4-130">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="f21c4-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="f21c4-131">-Name</span></span>
<span data-ttu-id="f21c4-132">Especifica o nome da nova conta local do Windows.</span><span class="sxs-lookup"><span data-stu-id="f21c4-132">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-133">-Senha</span><span class="sxs-lookup"><span data-stu-id="f21c4-133">-Password</span></span>
<span data-ttu-id="f21c4-134">Especifica a senha da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="f21c4-134">Specifies the user account password.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-135">-Poolid</span><span class="sxs-lookup"><span data-stu-id="f21c4-135">-PoolId</span></span>
<span data-ttu-id="f21c4-136">Especifica a ID do pool que contém o nó de computação no qual criar a conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="f21c4-136">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f21c4-137">-DefaultProfile</span></span>
<span data-ttu-id="f21c4-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f21c4-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f21c4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f21c4-139">CommonParameters</span></span>
<span data-ttu-id="f21c4-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f21c4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f21c4-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f21c4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f21c4-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f21c4-142">INPUTS</span></span>

### <span data-ttu-id="f21c4-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f21c4-143">BatchAccountContext</span></span>
<span data-ttu-id="f21c4-144">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f21c4-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="f21c4-145">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="f21c4-145">PSComputeNode</span></span>
<span data-ttu-id="f21c4-146">O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f21c4-146">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="f21c4-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f21c4-147">OUTPUTS</span></span>

## <span data-ttu-id="f21c4-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f21c4-148">NOTES</span></span>

## <span data-ttu-id="f21c4-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f21c4-149">RELATED LINKS</span></span>

[<span data-ttu-id="f21c4-150">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f21c4-150">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f21c4-151">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="f21c4-151">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="f21c4-152">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="f21c4-152">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="f21c4-153">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="f21c4-153">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


