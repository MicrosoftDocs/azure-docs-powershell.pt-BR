---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: d0f9e69ff36348cb4eb49920b85709b9b268adf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609841"
---
# <span data-ttu-id="ea2a9-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="ea2a9-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="ea2a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea2a9-103">Cria uma configuração de certificado de cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ea2a9-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea2a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea2a9-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea2a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea2a9-105">DESCRIPTION</span></span>
<span data-ttu-id="ea2a9-106">O cmdlet **New-AzureRmVmssVaultCertificateConfig** especifica o segredo que precisa ser colocado nas máquinas virtuais do VMSS (conjunto de escala de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="ea2a9-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="ea2a9-107">O resultado deste cmdlet destina-se a ser usado com o cmdlet Add-AzureRmVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="ea2a9-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="ea2a9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea2a9-108">EXAMPLES</span></span>

### <span data-ttu-id="ea2a9-109">Exemplo 1: criar uma configuração de certificado de cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="ea2a9-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="ea2a9-110">Esse comando cria uma configuração de certificado de cofre de chaves que usa o repositório de certificados chamado mycerts localizado na URL do certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="ea2a9-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="ea2a9-111">OS</span><span class="sxs-lookup"><span data-stu-id="ea2a9-111">PARAMETERS</span></span>

### <span data-ttu-id="ea2a9-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="ea2a9-112">-CertificateStore</span></span>
<span data-ttu-id="ea2a9-113">Especifica o repositório de certificados nas máquinas virtuais no conjunto de escala onde o certificado é adicionado.</span><span class="sxs-lookup"><span data-stu-id="ea2a9-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="ea2a9-114">Isso só é válido para conjuntos de escala da máquina virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="ea2a9-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea2a9-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="ea2a9-115">-CertificateUrl</span></span>
<span data-ttu-id="ea2a9-116">Especifica o URI de um certificado armazenado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ea2a9-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="ea2a9-117">É a codificação base64 do objeto JSON que é codificado em UTF-8: {"dados": " \<Base64-encoded-certificate\> ", "DataType": "pfx", "senha": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="ea2a9-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea2a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea2a9-118">-DefaultProfile</span></span>
<span data-ttu-id="ea2a9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea2a9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea2a9-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ea2a9-120">-Confirm</span></span>
<span data-ttu-id="ea2a9-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea2a9-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2a9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea2a9-122">-WhatIf</span></span>
<span data-ttu-id="ea2a9-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea2a9-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea2a9-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea2a9-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2a9-125">CommonParameters</span></span>
<span data-ttu-id="ea2a9-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea2a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2a9-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea2a9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2a9-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea2a9-128">INPUTS</span></span>

### <span data-ttu-id="ea2a9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ea2a9-129">System.String</span></span>

## <span data-ttu-id="ea2a9-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea2a9-130">OUTPUTS</span></span>

### <span data-ttu-id="ea2a9-131">Microsoft. Azure. Management. COMPUTE. Models. VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ea2a9-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="ea2a9-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea2a9-132">NOTES</span></span>

## <span data-ttu-id="ea2a9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea2a9-133">RELATED LINKS</span></span>

[<span data-ttu-id="ea2a9-134">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="ea2a9-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
