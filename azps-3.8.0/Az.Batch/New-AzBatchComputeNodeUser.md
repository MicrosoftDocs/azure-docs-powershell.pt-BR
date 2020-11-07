---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: 1aedf08bf6a9248b9cd3654471240a45b67ee893
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93947258"
---
# <span data-ttu-id="5e2ed-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="5e2ed-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="5e2ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e2ed-102">SYNOPSIS</span></span>
<span data-ttu-id="5e2ed-103">Cria uma conta de usuário em um nó de computação em lotes.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="5e2ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e2ed-104">SYNTAX</span></span>

### <span data-ttu-id="5e2ed-105">%</span><span class="sxs-lookup"><span data-stu-id="5e2ed-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e2ed-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e2ed-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e2ed-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e2ed-107">DESCRIPTION</span></span>
<span data-ttu-id="5e2ed-108">O cmdlet **New-AzBatchComputeNodeUser** cria uma conta de usuário em um nó de computação em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="5e2ed-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e2ed-109">EXAMPLES</span></span>

### <span data-ttu-id="5e2ed-110">Exemplo 1: criar uma conta de usuário que tenha credenciais administrativas</span><span class="sxs-lookup"><span data-stu-id="5e2ed-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="5e2ed-111">Esse comando cria uma conta de usuário no nó de computação que tem a ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="5e2ed-112">O nó está no pool que tem a ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="5e2ed-113">O nome de usuário é testuser, a senha é password, a conta expira em sete dias e a conta tem credenciais administrativas.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="5e2ed-114">Exemplo 2: criar uma conta de usuário em um nó de computação usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="5e2ed-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="5e2ed-115">Esse comando obtém o nó de computação chamado ComputeNode01 usando o cmdlet **Get-AzBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="5e2ed-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="5e2ed-116">Esse nó está no pool que tem a ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="5e2ed-117">O comando passa aquele nó COMPUTE para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5e2ed-118">O comando cria uma conta de usuário com o nome de usuário testuser e a senha da senha.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="5e2ed-119">OS</span><span class="sxs-lookup"><span data-stu-id="5e2ed-119">PARAMETERS</span></span>

### <span data-ttu-id="5e2ed-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5e2ed-120">-BatchContext</span></span>
<span data-ttu-id="5e2ed-121">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5e2ed-122">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5e2ed-123">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5e2ed-124">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5e2ed-125">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5e2ed-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="5e2ed-126">-ComputeNode</span></span>
<span data-ttu-id="5e2ed-127">Especifica o nó de computação, como um objeto **PSComputeNode** , em que esse cmdlet cria uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="5e2ed-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="5e2ed-128">-ComputeNodeId</span></span>
<span data-ttu-id="5e2ed-129">Especifica a ID do nó de computação em que esse cmdlet cria uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="5e2ed-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e2ed-130">-DefaultProfile</span></span>
<span data-ttu-id="5e2ed-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e2ed-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5e2ed-132">-ExpiryTime</span></span>
<span data-ttu-id="5e2ed-133">Especifica o tempo de expiração da nova conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="5e2ed-134">-ISAdmin</span><span class="sxs-lookup"><span data-stu-id="5e2ed-134">-IsAdmin</span></span>
<span data-ttu-id="5e2ed-135">Indica que o cmdlet cria uma conta de usuário que tem credenciais administrativas.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="5e2ed-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e2ed-136">-Name</span></span>
<span data-ttu-id="5e2ed-137">Especifica o nome da nova conta local do Windows.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-137">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="5e2ed-138">-Senha</span><span class="sxs-lookup"><span data-stu-id="5e2ed-138">-Password</span></span>
<span data-ttu-id="5e2ed-139">Especifica a senha da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-139">Specifies the user account password.</span></span>

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

### <span data-ttu-id="5e2ed-140">-Poolid</span><span class="sxs-lookup"><span data-stu-id="5e2ed-140">-PoolId</span></span>
<span data-ttu-id="5e2ed-141">Especifica a ID do pool que contém o nó de computação no qual criar a conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="5e2ed-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e2ed-142">CommonParameters</span></span>
<span data-ttu-id="5e2ed-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e2ed-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e2ed-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e2ed-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e2ed-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e2ed-145">INPUTS</span></span>

### <span data-ttu-id="5e2ed-146">Microsoft.Azure.Commands.Batch. Modelos. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="5e2ed-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="5e2ed-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5e2ed-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5e2ed-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e2ed-148">OUTPUTS</span></span>

### <span data-ttu-id="5e2ed-149">System. void</span><span class="sxs-lookup"><span data-stu-id="5e2ed-149">System.Void</span></span>

## <span data-ttu-id="5e2ed-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e2ed-150">NOTES</span></span>

## <span data-ttu-id="5e2ed-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e2ed-151">RELATED LINKS</span></span>

[<span data-ttu-id="5e2ed-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5e2ed-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5e2ed-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="5e2ed-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="5e2ed-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="5e2ed-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="5e2ed-155">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="5e2ed-155">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


