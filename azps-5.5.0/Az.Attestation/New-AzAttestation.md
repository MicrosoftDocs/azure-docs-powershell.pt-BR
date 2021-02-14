---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115536"
---
# <span data-ttu-id="db936-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="db936-101">New-AzAttestation</span></span>

## <span data-ttu-id="db936-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db936-102">SYNOPSIS</span></span>
<span data-ttu-id="db936-103">Cria um teste</span><span class="sxs-lookup"><span data-stu-id="db936-103">Creates an attestation</span></span>

## <span data-ttu-id="db936-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db936-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db936-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="db936-105">DESCRIPTION</span></span>
<span data-ttu-id="db936-106">O New-AzAttestation cmdlet cria um teste no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="db936-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="db936-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db936-107">EXAMPLES</span></span>

### <span data-ttu-id="db936-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db936-108">Example 1</span></span>
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

<span data-ttu-id="db936-109">Crie uma nova instância de um Provedor de Teste chamado *pshtest4* com algumas marcas e usando a confiança do AAD para dominar a política tee.</span><span class="sxs-lookup"><span data-stu-id="db936-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="db936-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="db936-110">Example 2</span></span>
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

<span data-ttu-id="db936-111">Crie uma nova instância de um Provedor de Teste chamado *pshtest3*' que usa a confiança isoladed para dominar a política TEE por meio da especificação de um conjunto de teclas de assinatura confiáveis por meio de um arquivo PEM.</span><span class="sxs-lookup"><span data-stu-id="db936-111">Create a new instance of an Attestation Provider named *pshtest3*\` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="db936-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db936-112">PARAMETERS</span></span>

### <span data-ttu-id="db936-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db936-113">-DefaultProfile</span></span>
<span data-ttu-id="db936-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db936-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db936-115">-Local</span><span class="sxs-lookup"><span data-stu-id="db936-115">-Location</span></span>
<span data-ttu-id="db936-116">Especifica a região do Azure na qual criar o provedor de teste.</span><span class="sxs-lookup"><span data-stu-id="db936-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="db936-117">Use o comando Get-AzResourceProvider com o parâmetro ProviderNamespace para ver suas opções.</span><span class="sxs-lookup"><span data-stu-id="db936-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="db936-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="db936-118">-Name</span></span>
<span data-ttu-id="db936-119">Especifica um nome da Instância a ser criado.</span><span class="sxs-lookup"><span data-stu-id="db936-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="db936-120">O nome pode ser qualquer combinação de letras, dígitos ou hífens.</span><span class="sxs-lookup"><span data-stu-id="db936-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="db936-121">O nome deve começar e terminar com uma letra ou dígito.</span><span class="sxs-lookup"><span data-stu-id="db936-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="db936-122">O nome deve ser universalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="db936-122">The name must be universally unique.</span></span>

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

### <span data-ttu-id="db936-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="db936-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="db936-124">Especifica o conjunto de chaves de assinatura confiáveis para política de emissão em um único arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="db936-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

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

### <span data-ttu-id="db936-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db936-125">-ResourceGroupName</span></span>
<span data-ttu-id="db936-126">Especifica o nome de um grupo de recursos existente no qual se cria o teste.</span><span class="sxs-lookup"><span data-stu-id="db936-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

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

### <span data-ttu-id="db936-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="db936-127">-Tag</span></span>
<span data-ttu-id="db936-128">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="db936-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="db936-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="db936-129">-Confirm</span></span>
<span data-ttu-id="db936-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db936-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db936-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db936-131">-WhatIf</span></span>
<span data-ttu-id="db936-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="db936-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db936-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db936-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db936-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db936-134">CommonParameters</span></span>
<span data-ttu-id="db936-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db936-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db936-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db936-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db936-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="db936-137">INPUTS</span></span>

### <span data-ttu-id="db936-138">System.String</span><span class="sxs-lookup"><span data-stu-id="db936-138">System.String</span></span>

### <span data-ttu-id="db936-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="db936-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="db936-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="db936-140">OUTPUTS</span></span>

### <span data-ttu-id="db936-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="db936-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="db936-142">Notas</span><span class="sxs-lookup"><span data-stu-id="db936-142">NOTES</span></span>

## <span data-ttu-id="db936-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db936-143">RELATED LINKS</span></span>
