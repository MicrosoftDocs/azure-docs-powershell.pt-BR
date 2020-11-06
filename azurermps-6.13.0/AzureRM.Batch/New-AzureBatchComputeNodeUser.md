---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 1e95eff4e93b1b7d55a099ad188fc196025cd06f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427298"
---
# <span data-ttu-id="41b3b-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="41b3b-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="41b3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="41b3b-103">Cria uma conta de usuário em um nó de computação em lotes.</span><span class="sxs-lookup"><span data-stu-id="41b3b-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41b3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41b3b-104">SYNTAX</span></span>

### <span data-ttu-id="41b3b-105">%</span><span class="sxs-lookup"><span data-stu-id="41b3b-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String>
 -Password <SecureString> [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41b3b-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="41b3b-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41b3b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41b3b-107">DESCRIPTION</span></span>
<span data-ttu-id="41b3b-108">O cmdlet **New-AzureBatchComputeNodeUser** cria uma conta de usuário em um nó de computação em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="41b3b-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="41b3b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41b3b-109">EXAMPLES</span></span>

### <span data-ttu-id="41b3b-110">Exemplo 1: criar uma conta de usuário que tenha credenciais administrativas</span><span class="sxs-lookup"><span data-stu-id="41b3b-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="41b3b-111">Esse comando cria uma conta de usuário no nó de computação que tem a ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="41b3b-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="41b3b-112">O nó está no pool que tem a ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="41b3b-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="41b3b-113">O nome de usuário é testuser, a senha é password, a conta expira em sete dias e a conta tem credenciais administrativas.</span><span class="sxs-lookup"><span data-stu-id="41b3b-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="41b3b-114">Exemplo 2: criar uma conta de usuário em um nó de computação usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="41b3b-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="41b3b-115">Esse comando obtém o nó de computação chamado ComputeNode01 usando o cmdlet **Get-AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="41b3b-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="41b3b-116">Esse nó está no pool que tem a ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="41b3b-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="41b3b-117">O comando passa aquele nó COMPUTE para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="41b3b-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="41b3b-118">O comando cria uma conta de usuário com o nome de usuário TestUserand a senha.</span><span class="sxs-lookup"><span data-stu-id="41b3b-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="41b3b-119">OS</span><span class="sxs-lookup"><span data-stu-id="41b3b-119">PARAMETERS</span></span>

### <span data-ttu-id="41b3b-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="41b3b-120">-BatchContext</span></span>
<span data-ttu-id="41b3b-121">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="41b3b-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="41b3b-122">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="41b3b-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="41b3b-123">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="41b3b-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="41b3b-124">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="41b3b-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="41b3b-125">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="41b3b-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="41b3b-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="41b3b-126">-ComputeNode</span></span>
<span data-ttu-id="41b3b-127">Especifica o nó de computação, como um objeto **PSComputeNode** , em que esse cmdlet cria uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="41b3b-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="41b3b-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="41b3b-128">-ComputeNodeId</span></span>
<span data-ttu-id="41b3b-129">Especifica a ID do nó de computação em que esse cmdlet cria uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="41b3b-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="41b3b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b3b-130">-DefaultProfile</span></span>
<span data-ttu-id="41b3b-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41b3b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41b3b-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="41b3b-132">-ExpiryTime</span></span>
<span data-ttu-id="41b3b-133">Especifica o tempo de expiração da nova conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="41b3b-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="41b3b-134">-ISAdmin</span><span class="sxs-lookup"><span data-stu-id="41b3b-134">-IsAdmin</span></span>
<span data-ttu-id="41b3b-135">Indica que o cmdlet cria uma conta de usuário que tem credenciais administrativas.</span><span class="sxs-lookup"><span data-stu-id="41b3b-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="41b3b-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="41b3b-136">-Name</span></span>
<span data-ttu-id="41b3b-137">Especifica o nome da nova conta local do Windows.</span><span class="sxs-lookup"><span data-stu-id="41b3b-137">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="41b3b-138">-Senha</span><span class="sxs-lookup"><span data-stu-id="41b3b-138">-Password</span></span>
<span data-ttu-id="41b3b-139">Especifica a senha da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="41b3b-139">Specifies the user account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b3b-140">-Poolid</span><span class="sxs-lookup"><span data-stu-id="41b3b-140">-PoolId</span></span>
<span data-ttu-id="41b3b-141">Especifica a ID do pool que contém o nó de computação no qual criar a conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="41b3b-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="41b3b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b3b-142">CommonParameters</span></span>
<span data-ttu-id="41b3b-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41b3b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b3b-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41b3b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b3b-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41b3b-145">INPUTS</span></span>

### <span data-ttu-id="41b3b-146">Microsoft.Azure.Commands.Batch. Modelos. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="41b3b-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="41b3b-147">Parâmetros: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="41b3b-147">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="41b3b-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="41b3b-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="41b3b-149">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="41b3b-149">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="41b3b-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41b3b-150">OUTPUTS</span></span>

### <span data-ttu-id="41b3b-151">System. void</span><span class="sxs-lookup"><span data-stu-id="41b3b-151">System.Void</span></span>

## <span data-ttu-id="41b3b-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41b3b-152">NOTES</span></span>

## <span data-ttu-id="41b3b-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41b3b-153">RELATED LINKS</span></span>

[<span data-ttu-id="41b3b-154">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="41b3b-154">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="41b3b-155">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="41b3b-155">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="41b3b-156">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="41b3b-156">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="41b3b-157">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="41b3b-157">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


