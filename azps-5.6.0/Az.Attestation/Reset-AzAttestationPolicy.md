---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: b628d93d44b863b4af05f09dd4d132ec986702e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887235"
---
# <span data-ttu-id="5a05a-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="5a05a-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="5a05a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a05a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a05a-103">Redefine a política de um locatário no Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="5a05a-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="5a05a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5a05a-104">SYNTAX</span></span>

### <span data-ttu-id="5a05a-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a05a-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a05a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a05a-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a05a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5a05a-107">DESCRIPTION</span></span>
<span data-ttu-id="5a05a-108">O Reset-AzAttestationPolicy cmdlet redefine a política de atestado definida pelo usuário de um locatário no Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="5a05a-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="5a05a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a05a-109">EXAMPLES</span></span>

### <span data-ttu-id="5a05a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5a05a-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="5a05a-111">Redefina a política para o padrão para o *pshtest* do Provedor de Atestados para O tipo de Tee *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="5a05a-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="5a05a-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5a05a-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="5a05a-113">Se o *pshtest* provedor de atestado estiver configurado para usar o modelo de confiança isolado, redefina a política como padrão para O tipo de Tee *SgxEnclave* incluindo uma política assinada.</span><span class="sxs-lookup"><span data-stu-id="5a05a-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="5a05a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5a05a-114">PARAMETERS</span></span>

### <span data-ttu-id="5a05a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a05a-115">-DefaultProfile</span></span>
<span data-ttu-id="5a05a-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a05a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a05a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5a05a-117">-Name</span></span>
<span data-ttu-id="5a05a-118">Especifica um nome do locatário.</span><span class="sxs-lookup"><span data-stu-id="5a05a-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="5a05a-119">Este cmdlet redefine a política de atestado para o locatário especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5a05a-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="5a05a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a05a-120">-PassThru</span></span>
<span data-ttu-id="5a05a-121">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="5a05a-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5a05a-122">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="5a05a-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5a05a-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="5a05a-123">-Policy</span></span>
<span data-ttu-id="5a05a-124">Especifica o Token Web JSON que descreve o documento de política a ser redefinido.</span><span class="sxs-lookup"><span data-stu-id="5a05a-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="5a05a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a05a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a05a-126">Especifica o nome do grupo de recursos de um provedor de atestados.</span><span class="sxs-lookup"><span data-stu-id="5a05a-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="5a05a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a05a-127">-ResourceId</span></span>
<span data-ttu-id="5a05a-128">Especifica o ResourceID de um provedor de atestados.</span><span class="sxs-lookup"><span data-stu-id="5a05a-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="5a05a-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="5a05a-129">-Tee</span></span>
<span data-ttu-id="5a05a-130">Especifica um tipo de Ambiente de Execução Confiável.</span><span class="sxs-lookup"><span data-stu-id="5a05a-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="5a05a-131">Suportamos quatro tipos de ambiente: SgxEnclave, OpenEnclave, CyResComponent e VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="5a05a-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="5a05a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a05a-132">-Confirm</span></span>
<span data-ttu-id="5a05a-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a05a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a05a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a05a-134">-WhatIf</span></span>
<span data-ttu-id="5a05a-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a05a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a05a-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a05a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a05a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a05a-137">CommonParameters</span></span>
<span data-ttu-id="5a05a-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a05a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a05a-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a05a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a05a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a05a-140">INPUTS</span></span>

### <span data-ttu-id="5a05a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5a05a-141">System.String</span></span>

## <span data-ttu-id="5a05a-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5a05a-142">OUTPUTS</span></span>

### <span data-ttu-id="5a05a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a05a-143">System.Boolean</span></span>

## <span data-ttu-id="5a05a-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="5a05a-144">NOTES</span></span>

## <span data-ttu-id="5a05a-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a05a-145">RELATED LINKS</span></span>
