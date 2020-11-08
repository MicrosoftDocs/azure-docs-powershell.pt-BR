---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110643"
---
# <span data-ttu-id="4923e-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="4923e-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="4923e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4923e-102">SYNOPSIS</span></span>
<span data-ttu-id="4923e-103">Redefine a política de um locatário no Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="4923e-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="4923e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4923e-104">SYNTAX</span></span>

### <span data-ttu-id="4923e-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4923e-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4923e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4923e-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4923e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4923e-107">DESCRIPTION</span></span>
<span data-ttu-id="4923e-108">O cmdlet Reset-AzAttestationPolicy redefine a política de atestado definida pelo usuário de um locatário no atestado do Azure.</span><span class="sxs-lookup"><span data-stu-id="4923e-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="4923e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4923e-109">EXAMPLES</span></span>

### <span data-ttu-id="4923e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4923e-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="4923e-111">Redefina a política para o padrão para o provedor de atestado *pshtest* para o tipo de *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="4923e-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="4923e-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4923e-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="4923e-113">Se o provedor de atestado *pshtest* estiver configurado para usar o modelo de confiança isolada, redefina a política para o padrão para o tipo de *SgxEnclave* , incluindo uma política assinada.</span><span class="sxs-lookup"><span data-stu-id="4923e-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="4923e-114">OS</span><span class="sxs-lookup"><span data-stu-id="4923e-114">PARAMETERS</span></span>

### <span data-ttu-id="4923e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4923e-115">-DefaultProfile</span></span>
<span data-ttu-id="4923e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4923e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4923e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4923e-117">-Name</span></span>
<span data-ttu-id="4923e-118">Especifica um nome do locatário.</span><span class="sxs-lookup"><span data-stu-id="4923e-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="4923e-119">Este cmdlet redefine a política de atestado para o locatário que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4923e-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4923e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4923e-120">-PassThru</span></span>
<span data-ttu-id="4923e-121">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="4923e-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4923e-122">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4923e-122">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4923e-123">-Política</span><span class="sxs-lookup"><span data-stu-id="4923e-123">-Policy</span></span>
<span data-ttu-id="4923e-124">Especifica o token da Web JSON que descreve o documento de política a ser redefinido.</span><span class="sxs-lookup"><span data-stu-id="4923e-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="4923e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4923e-125">-ResourceGroupName</span></span>
<span data-ttu-id="4923e-126">Especifica o nome do grupo de recursos de um provedor de atestado.</span><span class="sxs-lookup"><span data-stu-id="4923e-126">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4923e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4923e-127">-ResourceId</span></span>
<span data-ttu-id="4923e-128">Especifica o ResourceId de um provedor de atestado.</span><span class="sxs-lookup"><span data-stu-id="4923e-128">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4923e-129">-T</span><span class="sxs-lookup"><span data-stu-id="4923e-129">-Tee</span></span>
<span data-ttu-id="4923e-130">Especifica um tipo de ambiente de execução confiável.</span><span class="sxs-lookup"><span data-stu-id="4923e-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="4923e-131">Oferecemos suporte a quatro tipos de ambiente: SgxEnclave, OpenEnclave, CyResComponent e VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="4923e-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4923e-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4923e-132">-Confirm</span></span>
<span data-ttu-id="4923e-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4923e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4923e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4923e-134">-WhatIf</span></span>
<span data-ttu-id="4923e-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4923e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4923e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4923e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4923e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4923e-137">CommonParameters</span></span>
<span data-ttu-id="4923e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4923e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4923e-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4923e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4923e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4923e-140">INPUTS</span></span>

### <span data-ttu-id="4923e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4923e-141">System.String</span></span>

## <span data-ttu-id="4923e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4923e-142">OUTPUTS</span></span>

### <span data-ttu-id="4923e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4923e-143">System.Boolean</span></span>

## <span data-ttu-id="4923e-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4923e-144">NOTES</span></span>

## <span data-ttu-id="4923e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4923e-145">RELATED LINKS</span></span>
