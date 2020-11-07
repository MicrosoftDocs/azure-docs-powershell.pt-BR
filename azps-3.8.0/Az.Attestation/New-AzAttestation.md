---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942738"
---
# <span data-ttu-id="94cd6-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="94cd6-101">New-AzAttestation</span></span>

## <span data-ttu-id="94cd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="94cd6-103">Cria um atestado</span><span class="sxs-lookup"><span data-stu-id="94cd6-103">Creates an attestation</span></span>

## <span data-ttu-id="94cd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94cd6-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94cd6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94cd6-105">DESCRIPTION</span></span>
<span data-ttu-id="94cd6-106">O cmdlet New-AzAttestation cria um atestado no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="94cd6-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="94cd6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94cd6-107">EXAMPLES</span></span>

### <span data-ttu-id="94cd6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="94cd6-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest4 -ResourceGroupName psh-test-rg -Location "East US" -Tags @{Test="true";CreationYear="2020"}                                                                                                                                                                                         
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest4
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest4
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest4.us.attest.azure.net
Tags              : {CreationYear, Test}
TagsTable         :
                    Name          Value
                    ============  =====
                    CreationYear  2020
                    Test          true
```

<span data-ttu-id="94cd6-109">Crie uma nova instância de um provedor de atestado chamada *pshtest4* com algumas marcas e usando a relação de confiança AAD para a política de t-Mastering.</span><span class="sxs-lookup"><span data-stu-id="94cd6-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="94cd6-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="94cd6-110">Example 2</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg -Location "East US" -PolicySignersCertificateFile .\cert1.pem                                                                                                                                                
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest3
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest3
Status            : Ready
TrustModel        : Isolated
AttestUri         : https://pshtest3.us.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="94cd6-111">Crie uma nova instância de um provedor de atestado chamado *pshtest3* ' que usa a Isoladed confiança para a política de t-Mastering por meio da especificação de um conjunto de chaves de assinatura confiáveis por meio de um arquivo PEM.</span><span class="sxs-lookup"><span data-stu-id="94cd6-111">Create a new instance of an Attestation Provider named *pshtest3* \` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="94cd6-112">OS</span><span class="sxs-lookup"><span data-stu-id="94cd6-112">PARAMETERS</span></span>

### <span data-ttu-id="94cd6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94cd6-113">-DefaultProfile</span></span>
<span data-ttu-id="94cd6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94cd6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94cd6-115">-Local</span><span class="sxs-lookup"><span data-stu-id="94cd6-115">-Location</span></span>
<span data-ttu-id="94cd6-116">Especifica a região do Azure na qual criar o provedor de atestado.</span><span class="sxs-lookup"><span data-stu-id="94cd6-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="94cd6-117">Use o comando Get-AzResourceProvider com o parâmetro ProviderNamespace para ver suas opções.</span><span class="sxs-lookup"><span data-stu-id="94cd6-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94cd6-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="94cd6-118">-Name</span></span>
<span data-ttu-id="94cd6-119">Especifica um nome da instância a ser criada.</span><span class="sxs-lookup"><span data-stu-id="94cd6-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="94cd6-120">O nome pode ser qualquer combinação de letras, dígitos ou hifens.</span><span class="sxs-lookup"><span data-stu-id="94cd6-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="94cd6-121">O nome deve começar e terminar com uma letra ou um dígito.</span><span class="sxs-lookup"><span data-stu-id="94cd6-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="94cd6-122">O nome deve ser universalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="94cd6-122">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94cd6-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="94cd6-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="94cd6-124">Especifica o conjunto de chaves de assinatura confiáveis para a política de emissão em um único arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="94cd6-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94cd6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94cd6-125">-ResourceGroupName</span></span>
<span data-ttu-id="94cd6-126">Especifica o nome de um grupo de recursos existente no qual criar o atestado.</span><span class="sxs-lookup"><span data-stu-id="94cd6-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94cd6-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="94cd6-127">-Tag</span></span>
<span data-ttu-id="94cd6-128">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="94cd6-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94cd6-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="94cd6-129">-Confirm</span></span>
<span data-ttu-id="94cd6-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94cd6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94cd6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94cd6-131">-WhatIf</span></span>
<span data-ttu-id="94cd6-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94cd6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94cd6-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94cd6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94cd6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94cd6-134">CommonParameters</span></span>
<span data-ttu-id="94cd6-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94cd6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94cd6-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94cd6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94cd6-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94cd6-137">INPUTS</span></span>

### <span data-ttu-id="94cd6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="94cd6-138">System.String</span></span>

### <span data-ttu-id="94cd6-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="94cd6-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="94cd6-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94cd6-140">OUTPUTS</span></span>

### <span data-ttu-id="94cd6-141">Microsoft. Azure. Commands.. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="94cd6-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="94cd6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94cd6-142">NOTES</span></span>

## <span data-ttu-id="94cd6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94cd6-143">RELATED LINKS</span></span>
