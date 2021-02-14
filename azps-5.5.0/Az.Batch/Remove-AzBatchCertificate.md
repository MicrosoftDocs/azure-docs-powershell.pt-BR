---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 2f751a6efcf4b798c69bb0dfd9ecd38c33a65d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115524"
---
# <span data-ttu-id="96a4a-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="96a4a-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="96a4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="96a4a-103">Exclui um certificado de uma conta.</span><span class="sxs-lookup"><span data-stu-id="96a4a-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="96a4a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96a4a-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96a4a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="96a4a-105">DESCRIPTION</span></span>
<span data-ttu-id="96a4a-106">O cmdlet **Remove-AzBatchCertificate** remove um certificado da conta especificada do Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="96a4a-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="96a4a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96a4a-107">EXAMPLES</span></span>

### <span data-ttu-id="96a4a-108">Exemplo 1: Remover um certificado</span><span class="sxs-lookup"><span data-stu-id="96a4a-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="96a4a-109">Esse comando remove o certificado que tem a impressão digital especificada.</span><span class="sxs-lookup"><span data-stu-id="96a4a-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="96a4a-110">Exemplo 2:Remover todos os certificados ativos</span><span class="sxs-lookup"><span data-stu-id="96a4a-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="96a4a-111">Esse comando obtém todos os certificados que estão ativos usando o cmdlet Get-AzBatchCertificate dados.</span><span class="sxs-lookup"><span data-stu-id="96a4a-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="96a4a-112">O comando passa os certificados ativos para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="96a4a-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="96a4a-113">Esse cmdlet remove cada certificado.</span><span class="sxs-lookup"><span data-stu-id="96a4a-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="96a4a-114">O comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="96a4a-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="96a4a-115">Portanto, o comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="96a4a-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="96a4a-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96a4a-116">PARAMETERS</span></span>

### <span data-ttu-id="96a4a-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="96a4a-117">-BatchContext</span></span>
<span data-ttu-id="96a4a-118">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="96a4a-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="96a4a-119">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="96a4a-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="96a4a-120">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="96a4a-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="96a4a-121">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="96a4a-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="96a4a-122">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="96a4a-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="96a4a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a4a-123">-DefaultProfile</span></span>
<span data-ttu-id="96a4a-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="96a4a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96a4a-125">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="96a4a-125">-Thumbprint</span></span>
<span data-ttu-id="96a4a-126">Especifica a impressão digital do certificado que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="96a4a-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="96a4a-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="96a4a-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="96a4a-128">Especifica o algoritmo usado para derivar o parâmetro *Thumbprint.*</span><span class="sxs-lookup"><span data-stu-id="96a4a-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="96a4a-129">Atualmente, o único valor válido é sha1.</span><span class="sxs-lookup"><span data-stu-id="96a4a-129">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96a4a-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="96a4a-130">-Confirm</span></span>
<span data-ttu-id="96a4a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96a4a-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a4a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a4a-132">-WhatIf</span></span>
<span data-ttu-id="96a4a-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="96a4a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96a4a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96a4a-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a4a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a4a-135">CommonParameters</span></span>
<span data-ttu-id="96a4a-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a4a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a4a-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96a4a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a4a-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="96a4a-138">INPUTS</span></span>

### <span data-ttu-id="96a4a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="96a4a-139">System.String</span></span>

### <span data-ttu-id="96a4a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="96a4a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="96a4a-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="96a4a-141">OUTPUTS</span></span>

### <span data-ttu-id="96a4a-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="96a4a-142">System.Void</span></span>

## <span data-ttu-id="96a4a-143">Notas</span><span class="sxs-lookup"><span data-stu-id="96a4a-143">NOTES</span></span>

## <span data-ttu-id="96a4a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96a4a-144">RELATED LINKS</span></span>

[<span data-ttu-id="96a4a-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="96a4a-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="96a4a-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="96a4a-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="96a4a-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="96a4a-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="96a4a-148">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="96a4a-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="96a4a-149">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="96a4a-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
