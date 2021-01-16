---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 2f751a6efcf4b798c69bb0dfd9ecd38c33a65d01
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262802"
---
# <span data-ttu-id="1e5fc-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="1e5fc-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="1e5fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e5fc-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5fc-103">Exclui um certificado de uma conta.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="1e5fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e5fc-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e5fc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e5fc-105">DESCRIPTION</span></span>
<span data-ttu-id="1e5fc-106">O cmdlet **Remove-AzBatchCertificate** remove um certificado da conta em lotes do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="1e5fc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e5fc-107">EXAMPLES</span></span>

### <span data-ttu-id="1e5fc-108">Exemplo 1: remover um certificado</span><span class="sxs-lookup"><span data-stu-id="1e5fc-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="1e5fc-109">Esse comando Remove o certificado que tem a impressão digital especificada.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="1e5fc-110">Exemplo 2: remover todos os certificados ativos</span><span class="sxs-lookup"><span data-stu-id="1e5fc-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="1e5fc-111">Esse comando obtém todos os certificados ativos usando o cmdlet Get-AzBatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="1e5fc-112">O comando passa os certificados ativos para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1e5fc-113">Esse cmdlet Remove cada certificado.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="1e5fc-114">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="1e5fc-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="1e5fc-115">Portanto, o comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1e5fc-116">OS</span><span class="sxs-lookup"><span data-stu-id="1e5fc-116">PARAMETERS</span></span>

### <span data-ttu-id="1e5fc-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1e5fc-117">-BatchContext</span></span>
<span data-ttu-id="1e5fc-118">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1e5fc-119">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1e5fc-120">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1e5fc-121">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1e5fc-122">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1e5fc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5fc-123">-DefaultProfile</span></span>
<span data-ttu-id="1e5fc-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e5fc-125">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="1e5fc-125">-Thumbprint</span></span>
<span data-ttu-id="1e5fc-126">Especifica a impressão digital do certificado que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="1e5fc-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="1e5fc-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="1e5fc-128">Especifica o algoritmo usado para derivar o parâmetro de *impressão digital* .</span><span class="sxs-lookup"><span data-stu-id="1e5fc-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="1e5fc-129">No momento, o único valor válido é SHA1.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="1e5fc-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e5fc-130">-Confirm</span></span>
<span data-ttu-id="1e5fc-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e5fc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e5fc-132">-WhatIf</span></span>
<span data-ttu-id="1e5fc-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e5fc-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e5fc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5fc-135">CommonParameters</span></span>
<span data-ttu-id="1e5fc-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5fc-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e5fc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5fc-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e5fc-138">INPUTS</span></span>

### <span data-ttu-id="1e5fc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1e5fc-139">System.String</span></span>

### <span data-ttu-id="1e5fc-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1e5fc-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1e5fc-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e5fc-141">OUTPUTS</span></span>

### <span data-ttu-id="1e5fc-142">System. void</span><span class="sxs-lookup"><span data-stu-id="1e5fc-142">System.Void</span></span>

## <span data-ttu-id="1e5fc-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e5fc-143">NOTES</span></span>

## <span data-ttu-id="1e5fc-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e5fc-144">RELATED LINKS</span></span>

[<span data-ttu-id="1e5fc-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="1e5fc-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="1e5fc-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1e5fc-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1e5fc-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="1e5fc-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="1e5fc-148">Parar-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="1e5fc-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="1e5fc-149">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="1e5fc-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
