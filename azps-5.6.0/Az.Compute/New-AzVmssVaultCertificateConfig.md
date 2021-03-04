---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: cc607e12873e0b5b738a64d781d16ed73bc72f7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890008"
---
# <span data-ttu-id="792b0-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="792b0-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="792b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="792b0-102">SYNOPSIS</span></span>
<span data-ttu-id="792b0-103">Cria uma configuração de certificado do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="792b0-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="792b0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="792b0-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="792b0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="792b0-105">DESCRIPTION</span></span>
<span data-ttu-id="792b0-106">O cmdlet **New-AzVmssVaultCertificateConfig** especifica o segredo que precisa ser colocado nas máquinas virtuais do Conjunto de Escala de Máquina Virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="792b0-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="792b0-107">A saída desse cmdlet destina-se a ser usada com o cmdlet Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="792b0-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="792b0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="792b0-108">EXAMPLES</span></span>

### <span data-ttu-id="792b0-109">Exemplo 1: Criar uma configuração de certificado do Cofre de Chaves</span><span class="sxs-lookup"><span data-stu-id="792b0-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="792b0-110">Este comando cria uma configuração de certificado do Cofre de Chaves que usa o armazenamento de certificados chamado MyCerts localizado na URL de certificado especificada.</span><span class="sxs-lookup"><span data-stu-id="792b0-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="792b0-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="792b0-111">PARAMETERS</span></span>

### <span data-ttu-id="792b0-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="792b0-112">-CertificateStore</span></span>
<span data-ttu-id="792b0-113">Especifica o armazenamento de certificados nas máquinas virtuais no conjunto de escala onde o certificado é adicionado.</span><span class="sxs-lookup"><span data-stu-id="792b0-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="792b0-114">Isso só é válido para Conjuntos de Escala de Máquina Virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="792b0-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="792b0-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="792b0-115">-CertificateUrl</span></span>
<span data-ttu-id="792b0-116">Especifica o URI de um certificado armazenado no Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="792b0-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="792b0-117">É a codificação base64 do seguinte Objeto JSON que é codificada em UTF-8: { "data":" \<Base64-encoded-certificate\> ", "dataType":"pfx", "password":" \<pfx-file-password\> }</span><span class="sxs-lookup"><span data-stu-id="792b0-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="792b0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792b0-118">-DefaultProfile</span></span>
<span data-ttu-id="792b0-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="792b0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="792b0-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="792b0-120">-Confirm</span></span>
<span data-ttu-id="792b0-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="792b0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="792b0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="792b0-122">-WhatIf</span></span>
<span data-ttu-id="792b0-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="792b0-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="792b0-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="792b0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="792b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792b0-125">CommonParameters</span></span>
<span data-ttu-id="792b0-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="792b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792b0-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="792b0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792b0-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="792b0-128">INPUTS</span></span>

### <span data-ttu-id="792b0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="792b0-129">System.String</span></span>

## <span data-ttu-id="792b0-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="792b0-130">OUTPUTS</span></span>

### <span data-ttu-id="792b0-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="792b0-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="792b0-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="792b0-132">NOTES</span></span>

## <span data-ttu-id="792b0-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="792b0-133">RELATED LINKS</span></span>

[<span data-ttu-id="792b0-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="792b0-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
