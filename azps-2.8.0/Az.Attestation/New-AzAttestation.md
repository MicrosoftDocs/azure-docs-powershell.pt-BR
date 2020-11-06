---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: ce21b116ceb41bfdfb26008dd44c914f3198ab39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597883"
---
# <span data-ttu-id="a97ab-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="a97ab-101">New-AzAttestation</span></span>

## <span data-ttu-id="a97ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a97ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a97ab-103">Cria um atestado</span><span class="sxs-lookup"><span data-stu-id="a97ab-103">Creates an attestation</span></span>

## <span data-ttu-id="a97ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a97ab-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> [-AttestationPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a97ab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a97ab-105">DESCRIPTION</span></span>
<span data-ttu-id="a97ab-106">O cmdlet New-AzAttestation cria um atestado no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="a97ab-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="a97ab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a97ab-107">EXAMPLES</span></span>

### <span data-ttu-id="a97ab-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a97ab-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```

<span data-ttu-id="a97ab-109">Criar um novo atestado "exemplo" na assinatura atual, grupo de recursos "Rg1"</span><span class="sxs-lookup"><span data-stu-id="a97ab-109">Create a new Attestation "example" in current Subscription, Resource Group "rg1"</span></span>

## <span data-ttu-id="a97ab-110">OS</span><span class="sxs-lookup"><span data-stu-id="a97ab-110">PARAMETERS</span></span>

### <span data-ttu-id="a97ab-111">-AttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="a97ab-111">-AttestationPolicy</span></span>
<span data-ttu-id="a97ab-112">Especifica a política de atestado aprovada na qual criar o atestado.</span><span class="sxs-lookup"><span data-stu-id="a97ab-112">Specifies the attestation policy passed in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a97ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a97ab-113">-DefaultProfile</span></span>
<span data-ttu-id="a97ab-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a97ab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a97ab-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a97ab-115">-Name</span></span>
<span data-ttu-id="a97ab-116">Especifica um nome da instância a ser criada.</span><span class="sxs-lookup"><span data-stu-id="a97ab-116">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="a97ab-117">O nome pode ser qualquer combinação de letras, dígitos ou hifens.</span><span class="sxs-lookup"><span data-stu-id="a97ab-117">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="a97ab-118">O nome deve começar e terminar com uma letra ou um dígito.</span><span class="sxs-lookup"><span data-stu-id="a97ab-118">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="a97ab-119">O nome deve ser universalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a97ab-119">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a97ab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a97ab-120">-ResourceGroupName</span></span>
<span data-ttu-id="a97ab-121">Especifica o nome de um grupo de recursos existente no qual criar o atestado.</span><span class="sxs-lookup"><span data-stu-id="a97ab-121">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a97ab-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a97ab-122">-Confirm</span></span>
<span data-ttu-id="a97ab-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a97ab-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a97ab-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a97ab-124">-WhatIf</span></span>
<span data-ttu-id="a97ab-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a97ab-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a97ab-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a97ab-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a97ab-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a97ab-127">CommonParameters</span></span>
<span data-ttu-id="a97ab-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a97ab-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a97ab-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a97ab-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a97ab-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a97ab-130">INPUTS</span></span>

### <span data-ttu-id="a97ab-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a97ab-131">System.String</span></span>

## <span data-ttu-id="a97ab-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a97ab-132">OUTPUTS</span></span>

### <span data-ttu-id="a97ab-133">Microsoft. Azure. Commands.. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="a97ab-133">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="a97ab-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a97ab-134">NOTES</span></span>

## <span data-ttu-id="a97ab-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a97ab-135">RELATED LINKS</span></span>
