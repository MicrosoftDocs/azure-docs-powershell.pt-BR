---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssvaultcertificateconfig
schema: 2.0.0
ms.openlocfilehash: 9ae4e22cde856129d21965b7e7f2fc9af647572a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786157"
---
# <span data-ttu-id="a2c7c-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="a2c7c-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="a2c7c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2c7c-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c7c-103">Cria uma configuração de certificado de cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2c7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2c7c-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2c7c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2c7c-105">DESCRIPTION</span></span>
<span data-ttu-id="a2c7c-106">O cmdlet **New-AzureRmVmssVaultCertificateConfig** especifica o segredo que precisa ser colocado nas máquinas virtuais do VMSS (conjunto de escala de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="a2c7c-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="a2c7c-107">O resultado deste cmdlet destina-se a ser usado com o cmdlet Add-AzureRmVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="a2c7c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2c7c-108">EXAMPLES</span></span>

### <span data-ttu-id="a2c7c-109">Exemplo 1: criar uma configuração de certificado de cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="a2c7c-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="a2c7c-110">Esse comando cria uma configuração de certificado de cofre de chaves que usa o repositório de certificados chamado mycerts localizado na URL do certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="a2c7c-111">OS</span><span class="sxs-lookup"><span data-stu-id="a2c7c-111">PARAMETERS</span></span>

### <span data-ttu-id="a2c7c-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="a2c7c-112">-CertificateStore</span></span>
<span data-ttu-id="a2c7c-113">Especifica o repositório de certificados nas máquinas virtuais no conjunto de escala onde o certificado é adicionado.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="a2c7c-114">Isso só é válido para conjuntos de escala da máquina virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c7c-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="a2c7c-115">-CertificateUrl</span></span>
<span data-ttu-id="a2c7c-116">Especifica o URI de um certificado armazenado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="a2c7c-117">É a codificação base64 do objeto JSON que é codificado em UTF-8:</span><span class="sxs-lookup"><span data-stu-id="a2c7c-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="a2c7c-118">{"dados": " \<Base64-encoded-certificate\> ", "tipo de dados": "pfx", "senha": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="a2c7c-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c7c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c7c-119">-DefaultProfile</span></span>
<span data-ttu-id="a2c7c-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2c7c-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a2c7c-121">-Confirm</span></span>
<span data-ttu-id="a2c7c-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c7c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2c7c-123">-WhatIf</span></span>
<span data-ttu-id="a2c7c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2c7c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c7c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c7c-126">CommonParameters</span></span>
<span data-ttu-id="a2c7c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c7c-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2c7c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c7c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2c7c-129">INPUTS</span></span>

### <span data-ttu-id="a2c7c-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a2c7c-130">None</span></span>
<span data-ttu-id="a2c7c-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a2c7c-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2c7c-132">OUTPUTS</span></span>

###  
<span data-ttu-id="a2c7c-133">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a2c7c-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a2c7c-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2c7c-134">NOTES</span></span>

## <span data-ttu-id="a2c7c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2c7c-135">RELATED LINKS</span></span>

[<span data-ttu-id="a2c7c-136">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="a2c7c-136">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
