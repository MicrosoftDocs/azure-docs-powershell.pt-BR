---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: e62aebd6a03f7d5a162f141eae55e3df6c9a0a88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440128"
---
# <span data-ttu-id="f69b7-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f69b7-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="f69b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f69b7-102">SYNOPSIS</span></span>
<span data-ttu-id="f69b7-103">Exclui um certificado de uma conta.</span><span class="sxs-lookup"><span data-stu-id="f69b7-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f69b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f69b7-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f69b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f69b7-105">DESCRIPTION</span></span>
<span data-ttu-id="f69b7-106">O cmdlet **Remove-AzureBatchCertificate** remove um certificado da conta em lotes do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="f69b7-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="f69b7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f69b7-107">EXAMPLES</span></span>

### <span data-ttu-id="f69b7-108">Exemplo 1: remover um certificado</span><span class="sxs-lookup"><span data-stu-id="f69b7-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="f69b7-109">Esse comando Remove o certificado que tem a impressão digital especificada.</span><span class="sxs-lookup"><span data-stu-id="f69b7-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="f69b7-110">Exemplo 2: remover todos os certificados ativos</span><span class="sxs-lookup"><span data-stu-id="f69b7-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="f69b7-111">Esse comando obtém todos os certificados ativos usando o cmdlet Get-AzureBatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="f69b7-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="f69b7-112">O comando passa os certificados ativos para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="f69b7-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f69b7-113">Esse cmdlet Remove cada certificado.</span><span class="sxs-lookup"><span data-stu-id="f69b7-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="f69b7-114">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="f69b7-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f69b7-115">Portanto, o comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="f69b7-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f69b7-116">OS</span><span class="sxs-lookup"><span data-stu-id="f69b7-116">PARAMETERS</span></span>

### <span data-ttu-id="f69b7-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f69b7-117">-BatchContext</span></span>
<span data-ttu-id="f69b7-118">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="f69b7-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f69b7-119">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="f69b7-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f69b7-120">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="f69b7-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f69b7-121">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="f69b7-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f69b7-122">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f69b7-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f69b7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f69b7-123">-DefaultProfile</span></span>
<span data-ttu-id="f69b7-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f69b7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f69b7-125">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="f69b7-125">-Thumbprint</span></span>
<span data-ttu-id="f69b7-126">Especifica a impressão digital do certificado que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="f69b7-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69b7-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f69b7-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="f69b7-128">Especifica o algoritmo usado para derivar o parâmetro de *impressão digital* .</span><span class="sxs-lookup"><span data-stu-id="f69b7-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="f69b7-129">No momento, o único valor válido é SHA1.</span><span class="sxs-lookup"><span data-stu-id="f69b7-129">Currently, the only valid value is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69b7-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f69b7-130">-Confirm</span></span>
<span data-ttu-id="f69b7-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f69b7-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f69b7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f69b7-132">-WhatIf</span></span>
<span data-ttu-id="f69b7-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f69b7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f69b7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f69b7-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f69b7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69b7-135">CommonParameters</span></span>
<span data-ttu-id="f69b7-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f69b7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69b7-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f69b7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69b7-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f69b7-138">INPUTS</span></span>

### <span data-ttu-id="f69b7-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f69b7-139">BatchAccountContext</span></span>
<span data-ttu-id="f69b7-140">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f69b7-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="f69b7-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f69b7-141">OUTPUTS</span></span>

## <span data-ttu-id="f69b7-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f69b7-142">NOTES</span></span>

## <span data-ttu-id="f69b7-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f69b7-143">RELATED LINKS</span></span>

[<span data-ttu-id="f69b7-144">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f69b7-144">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="f69b7-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f69b7-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f69b7-146">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f69b7-146">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="f69b7-147">Parar-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="f69b7-147">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="f69b7-148">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="f69b7-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


