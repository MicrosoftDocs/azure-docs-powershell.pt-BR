---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
ms.openlocfilehash: 26bd35f59ae5e640093c1695e7caf991e1e1e956
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430516"
---
# <span data-ttu-id="ae7a4-101">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ae7a4-101">Get-AzBatchCertificate</span></span>

## <span data-ttu-id="ae7a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae7a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7a4-103">Obtém os certificados em uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-103">Gets the certificates in a Batch account.</span></span>

## <span data-ttu-id="ae7a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae7a4-104">SYNTAX</span></span>

### <span data-ttu-id="ae7a4-105">ODataFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae7a4-105">ODataFilter (Default)</span></span>
```
Get-AzBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae7a4-106">Digital</span><span class="sxs-lookup"><span data-stu-id="ae7a4-106">Thumbprint</span></span>
```
Get-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae7a4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae7a4-107">DESCRIPTION</span></span>
<span data-ttu-id="ae7a4-108">O cmdlet **Get-AzBatchCertificate** Obtém os certificados na conta em lotes do Azure que o parâmetro *BatchContext* especifica.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-108">The **Get-AzBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="ae7a4-109">Para obter um certificado específico, especifique os parâmetros de *ThumbprintAlgorithm* e *impressão digital* .</span><span class="sxs-lookup"><span data-stu-id="ae7a4-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="ae7a4-110">Especifique o parâmetro *Filter* para obter os certificados correspondentes a um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="ae7a4-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="ae7a4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae7a4-111">EXAMPLES</span></span>

### <span data-ttu-id="ae7a4-112">Exemplo 1: obter um certificado por impressão digital</span><span class="sxs-lookup"><span data-stu-id="ae7a4-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=C1E494A415149C5F211C4778B52F2E834A07247
C)
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               :
PreviousStateTransitionTime :
Data                        :
CertificateFormat           :
Password                    :
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="ae7a4-113">Esse comando obtém um único certificado que tem a impressão digital especificada.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="ae7a4-114">O algoritmo de impressão digital do certificado é SHA1.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="ae7a4-115">Exemplo 2: obter certificados filtrados</span><span class="sxs-lookup"><span data-stu-id="ae7a4-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
Thumbprint                  : 025b351b087a084c5067f5e71eff8591970323f9
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=025b351b087a084c5067f5e71eff8591970323f9)
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:17 PM
PreviousState               :
PreviousStateTransitionTime :
Data                        :
CertificateFormat           :
Password                    :
PublicData                  : MIIB9DCCAWGgAwIBAgIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAyMB4XDTE1MTAwMjE2MjkxNFoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDIwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAJxagvVrlnKfv6hfzSiFJUkdGkPjC3tFiKebK6IaeHzesFdFfupXUE
wT0xOWh9xwa3OVkPECEc/u1sw3iVX/J4AODiwzmOWutoVRpWjxGFpgw9+dPvXMjs/Ue7JL7ag3siHs5EcarW91qKbgtko6i/r4emaRyk60U93TrbWQAWJ9AgMBAAGjS
zBJMEcGA1UdAQRAMD6AEAdqsOpyeXF/uDe7ZGKeez+hGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMoIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAA4GBAC0MaAem
6ByyURFvGnFZyjEepjXC5wcaGq+gguDFe8rG88ceig1ZqewdcmC1y4p05uBhbmETbYVWzJarNsHYq2LTihi4t2J4jt2YVYz/IRdUB82iaFFbJRSPrN+6xD3KM2lve5N
4OjtlZAdiXiSUYFf3I6ypberUsAdba3QQajCN
DeleteCertificateError      :

Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=c1e494a415149c5f211c4778b52f2e834a07247c)
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               :
PreviousStateTransitionTime :
Data                        :
CertificateFormat           :
Password                    :
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="ae7a4-116">Esse comando obtém todos os certificados no estado ativo da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="ae7a4-117">O parâmetro *Filter* especifica o estado.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="ae7a4-118">OS</span><span class="sxs-lookup"><span data-stu-id="ae7a4-118">PARAMETERS</span></span>

### <span data-ttu-id="ae7a4-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ae7a4-119">-BatchContext</span></span>
<span data-ttu-id="ae7a4-120">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ae7a4-121">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ae7a4-122">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ae7a4-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ae7a4-124">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ae7a4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae7a4-125">-DefaultProfile</span></span>
<span data-ttu-id="ae7a4-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae7a4-127">-Filtro</span><span class="sxs-lookup"><span data-stu-id="ae7a4-127">-Filter</span></span>
<span data-ttu-id="ae7a4-128">Especifica uma cláusula de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="ae7a4-129">Se você especificar esse parâmetro, esse cmdlet obterá os certificados que correspondem ao filtro.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7a4-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ae7a4-130">-MaxCount</span></span>
<span data-ttu-id="ae7a4-131">Especifica o número máximo de certificados a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="ae7a4-132">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ae7a4-133">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-133">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7a4-134">-Selecione</span><span class="sxs-lookup"><span data-stu-id="ae7a4-134">-Select</span></span>
<span data-ttu-id="ae7a4-135">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="ae7a4-136">Especifique um valor para esse parâmetro para obter propriedades específicas em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7a4-137">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="ae7a4-137">-Thumbprint</span></span>
<span data-ttu-id="ae7a4-138">Especifica a impressão digital do certificado que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7a4-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ae7a4-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="ae7a4-140">Especifica o algoritmo usado para derivar o parâmetro de *impressão digital* .</span><span class="sxs-lookup"><span data-stu-id="ae7a4-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="ae7a4-141">No momento, o único valor válido é SHA1.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-141">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7a4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7a4-142">CommonParameters</span></span>
<span data-ttu-id="ae7a4-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae7a4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7a4-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae7a4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7a4-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae7a4-145">INPUTS</span></span>

### <span data-ttu-id="ae7a4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ae7a4-146">System.String</span></span>

### <span data-ttu-id="ae7a4-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ae7a4-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ae7a4-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae7a4-148">OUTPUTS</span></span>

### <span data-ttu-id="ae7a4-149">Microsoft.Azure.Commands.Batch. Modelos. PSCertificate</span><span class="sxs-lookup"><span data-stu-id="ae7a4-149">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="ae7a4-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae7a4-150">NOTES</span></span>

## <span data-ttu-id="ae7a4-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae7a4-151">RELATED LINKS</span></span>

[<span data-ttu-id="ae7a4-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ae7a4-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ae7a4-153">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ae7a4-153">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="ae7a4-154">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ae7a4-154">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="ae7a4-155">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="ae7a4-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
