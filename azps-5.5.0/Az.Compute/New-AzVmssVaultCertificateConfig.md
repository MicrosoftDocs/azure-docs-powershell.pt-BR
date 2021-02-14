---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 23b2b3acd5bb15771d3383cc39c6e0a69073a750
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111126"
---
# <span data-ttu-id="b6907-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="b6907-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="b6907-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6907-102">SYNOPSIS</span></span>
<span data-ttu-id="b6907-103">Cria uma configuração de certificado do Cofre de Chave.</span><span class="sxs-lookup"><span data-stu-id="b6907-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="b6907-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6907-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6907-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6907-105">DESCRIPTION</span></span>
<span data-ttu-id="b6907-106">O cmdlet **New-AzVmssVaultCertificateConfig** especifica o segredo que precisa ser colocado nas máquinas virtuais VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="b6907-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="b6907-107">A saída deste cmdlet destina-se a ser usada com Add-AzVmssSecret cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6907-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="b6907-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6907-108">EXAMPLES</span></span>

### <span data-ttu-id="b6907-109">Exemplo 1: Criar uma configuração de certificado do Cofre de Chave</span><span class="sxs-lookup"><span data-stu-id="b6907-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="b6907-110">Esse comando cria uma configuração de certificado do Cofre de Chave que usa o armazenamento de certificados chamado MyCerts localizado na URL de certificado especificada.</span><span class="sxs-lookup"><span data-stu-id="b6907-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="b6907-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6907-111">PARAMETERS</span></span>

### <span data-ttu-id="b6907-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="b6907-112">-CertificateStore</span></span>
<span data-ttu-id="b6907-113">Especifica o armazenamento de certificados nas máquinas virtuais no conjunto de escala onde o certificado é adicionado.</span><span class="sxs-lookup"><span data-stu-id="b6907-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="b6907-114">Isso só é válido para Conjuntos de Escala de Máquina Virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="b6907-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="b6907-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="b6907-115">-CertificateUrl</span></span>
<span data-ttu-id="b6907-116">Especifica o URI de um certificado armazenado no Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="b6907-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="b6907-117">É a codificação de base64 do seguinte Objeto JSON codificada em UTF-8: { "dados":" \<Base64-encoded-certificate\> ", "dataType":"pfx", "password":" \<pfx-file-password\> }</span><span class="sxs-lookup"><span data-stu-id="b6907-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="b6907-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6907-118">-DefaultProfile</span></span>
<span data-ttu-id="b6907-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b6907-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6907-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b6907-120">-Confirm</span></span>
<span data-ttu-id="b6907-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6907-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6907-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6907-122">-WhatIf</span></span>
<span data-ttu-id="b6907-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b6907-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6907-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6907-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6907-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6907-125">CommonParameters</span></span>
<span data-ttu-id="b6907-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6907-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6907-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6907-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6907-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="b6907-128">INPUTS</span></span>

### <span data-ttu-id="b6907-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b6907-129">System.String</span></span>

## <span data-ttu-id="b6907-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="b6907-130">OUTPUTS</span></span>

### <span data-ttu-id="b6907-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b6907-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="b6907-132">Notas</span><span class="sxs-lookup"><span data-stu-id="b6907-132">NOTES</span></span>

## <span data-ttu-id="b6907-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6907-133">RELATED LINKS</span></span>

[<span data-ttu-id="b6907-134">Add-AzVmssSecsec</span><span class="sxs-lookup"><span data-stu-id="b6907-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
