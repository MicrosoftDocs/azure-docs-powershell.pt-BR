---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c32a9e2fd474578c8526c8352e8649cb84d8b016
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887234"
---
# <span data-ttu-id="059b2-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="059b2-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="059b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059b2-102">SYNOPSIS</span></span>
<span data-ttu-id="059b2-103">Define a política de um locatário no Azure Attestationn.</span><span class="sxs-lookup"><span data-stu-id="059b2-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="059b2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="059b2-104">SYNTAX</span></span>

### <span data-ttu-id="059b2-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="059b2-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="059b2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="059b2-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="059b2-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="059b2-107">DESCRIPTION</span></span>
<span data-ttu-id="059b2-108">O Set-AzAttestationPolicy cmdlet define a política de um locatário no Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="059b2-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="059b2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="059b2-109">EXAMPLES</span></span>

### <span data-ttu-id="059b2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="059b2-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="059b2-111">Define a política definida pelo usuário para o tipo TEE *SgxEnclave* para *pshtest* do Provedor de Atestado usando um formato de política de texto (padrão).</span><span class="sxs-lookup"><span data-stu-id="059b2-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="059b2-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="059b2-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="059b2-113">Define a política definida pelo usuário para o tipo TEE *SgxEnclave* para *pshtest* do Provedor de Atestado usando um formato de política JWT.</span><span class="sxs-lookup"><span data-stu-id="059b2-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="059b2-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="059b2-114">PARAMETERS</span></span>

### <span data-ttu-id="059b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059b2-115">-DefaultProfile</span></span>
<span data-ttu-id="059b2-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="059b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="059b2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="059b2-117">-Name</span></span>
<span data-ttu-id="059b2-118">Especifica um nome do locatário.</span><span class="sxs-lookup"><span data-stu-id="059b2-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="059b2-119">Este cmdlet define a política de atestado para o locatário especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="059b2-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="059b2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="059b2-120">-PassThru</span></span>
<span data-ttu-id="059b2-121">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="059b2-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="059b2-122">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="059b2-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="059b2-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="059b2-123">-Policy</span></span>
<span data-ttu-id="059b2-124">Especifica o documento de política a ser definido.</span><span class="sxs-lookup"><span data-stu-id="059b2-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="059b2-125">O formato de política pode ser Text ou JSON Web Token (JWT).</span><span class="sxs-lookup"><span data-stu-id="059b2-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="059b2-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="059b2-126">-PolicyFormat</span></span>
<span data-ttu-id="059b2-127">Especifica o formato da política, Text ou JWT (JSON Web Token).</span><span class="sxs-lookup"><span data-stu-id="059b2-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="059b2-128">O formato de política padrão é Text.</span><span class="sxs-lookup"><span data-stu-id="059b2-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="059b2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="059b2-129">-ResourceGroupName</span></span>
<span data-ttu-id="059b2-130">Especifica o nome do grupo de recursos de um provedor de atestados.</span><span class="sxs-lookup"><span data-stu-id="059b2-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="059b2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="059b2-131">-ResourceId</span></span>
<span data-ttu-id="059b2-132">Especifica o ResourceID de um provedor de atestados.</span><span class="sxs-lookup"><span data-stu-id="059b2-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="059b2-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="059b2-133">-Tee</span></span>
<span data-ttu-id="059b2-134">Especifica um tipo de Ambiente de Execução Confiável.</span><span class="sxs-lookup"><span data-stu-id="059b2-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="059b2-135">Há suporte para quatro tipos de ambiente: SgxEnclave, OpenEnclave, CyResComponent e VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="059b2-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="059b2-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="059b2-136">-Confirm</span></span>
<span data-ttu-id="059b2-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="059b2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="059b2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059b2-138">-WhatIf</span></span>
<span data-ttu-id="059b2-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="059b2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="059b2-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="059b2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="059b2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059b2-141">CommonParameters</span></span>
<span data-ttu-id="059b2-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="059b2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059b2-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="059b2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059b2-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="059b2-144">INPUTS</span></span>

### <span data-ttu-id="059b2-145">System.String</span><span class="sxs-lookup"><span data-stu-id="059b2-145">System.String</span></span>

## <span data-ttu-id="059b2-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="059b2-146">OUTPUTS</span></span>

### <span data-ttu-id="059b2-147">System.String</span><span class="sxs-lookup"><span data-stu-id="059b2-147">System.String</span></span>

## <span data-ttu-id="059b2-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="059b2-148">NOTES</span></span>

## <span data-ttu-id="059b2-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="059b2-149">RELATED LINKS</span></span>
