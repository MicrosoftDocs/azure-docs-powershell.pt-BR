---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 23b2b3acd5bb15771d3383cc39c6e0a69073a750
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113108"
---
# <span data-ttu-id="9501e-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="9501e-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="9501e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9501e-102">SYNOPSIS</span></span>
<span data-ttu-id="9501e-103">Cria uma configuração de certificado de cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="9501e-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="9501e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9501e-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9501e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9501e-105">DESCRIPTION</span></span>
<span data-ttu-id="9501e-106">O cmdlet **New-AzVmssVaultCertificateConfig** especifica o segredo que precisa ser colocado nas máquinas virtuais do VMSS (conjunto de escala de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="9501e-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="9501e-107">O resultado deste cmdlet destina-se a ser usado com o cmdlet Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="9501e-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="9501e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9501e-108">EXAMPLES</span></span>

### <span data-ttu-id="9501e-109">Exemplo 1: criar uma configuração de certificado de cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="9501e-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="9501e-110">Esse comando cria uma configuração de certificado de cofre de chaves que usa o repositório de certificados chamado mycerts localizado na URL do certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="9501e-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="9501e-111">OS</span><span class="sxs-lookup"><span data-stu-id="9501e-111">PARAMETERS</span></span>

### <span data-ttu-id="9501e-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="9501e-112">-CertificateStore</span></span>
<span data-ttu-id="9501e-113">Especifica o repositório de certificados nas máquinas virtuais no conjunto de escala onde o certificado é adicionado.</span><span class="sxs-lookup"><span data-stu-id="9501e-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="9501e-114">Isso só é válido para conjuntos de escala da máquina virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="9501e-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="9501e-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="9501e-115">-CertificateUrl</span></span>
<span data-ttu-id="9501e-116">Especifica o URI de um certificado armazenado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="9501e-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="9501e-117">É a codificação base64 do objeto JSON que é codificado em UTF-8: {"dados": " \<Base64-encoded-certificate\> ", "DataType": "pfx", "senha": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="9501e-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="9501e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9501e-118">-DefaultProfile</span></span>
<span data-ttu-id="9501e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9501e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9501e-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9501e-120">-Confirm</span></span>
<span data-ttu-id="9501e-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9501e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9501e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9501e-122">-WhatIf</span></span>
<span data-ttu-id="9501e-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9501e-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9501e-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9501e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9501e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9501e-125">CommonParameters</span></span>
<span data-ttu-id="9501e-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9501e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9501e-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9501e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9501e-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9501e-128">INPUTS</span></span>

### <span data-ttu-id="9501e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9501e-129">System.String</span></span>

## <span data-ttu-id="9501e-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9501e-130">OUTPUTS</span></span>

### <span data-ttu-id="9501e-131">Microsoft. Azure. Management. COMPUTE. Models. VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="9501e-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="9501e-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9501e-132">NOTES</span></span>

## <span data-ttu-id="9501e-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9501e-133">RELATED LINKS</span></span>

[<span data-ttu-id="9501e-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="9501e-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
