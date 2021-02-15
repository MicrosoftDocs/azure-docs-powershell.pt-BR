---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112266"
---
# <span data-ttu-id="98ec1-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="98ec1-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="98ec1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="98ec1-103">Define a política de um locatário no Azure Attestationn.</span><span class="sxs-lookup"><span data-stu-id="98ec1-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="98ec1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98ec1-104">SYNTAX</span></span>

### <span data-ttu-id="98ec1-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="98ec1-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98ec1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98ec1-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98ec1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="98ec1-107">DESCRIPTION</span></span>
<span data-ttu-id="98ec1-108">O Set-AzAttestationPolicy cmdlet define a política de um locatário no Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="98ec1-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="98ec1-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="98ec1-109">EXAMPLES</span></span>

### <span data-ttu-id="98ec1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98ec1-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="98ec1-111">Define a política definida pelo usuário para o tipo de TEE *SgxEnmaxe* para teste pshtest do Provedor de Teste de *Attestation* usando um formato de política de texto (padrão).</span><span class="sxs-lookup"><span data-stu-id="98ec1-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="98ec1-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="98ec1-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="98ec1-113">Define a política definida pelo usuário para o tipo de TEE *SgxEnmaxe* para teste *pshtest* do Provedor de Teste usando um formato de política JWT.</span><span class="sxs-lookup"><span data-stu-id="98ec1-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="98ec1-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98ec1-114">PARAMETERS</span></span>

### <span data-ttu-id="98ec1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ec1-115">-DefaultProfile</span></span>
<span data-ttu-id="98ec1-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98ec1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98ec1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="98ec1-117">-Name</span></span>
<span data-ttu-id="98ec1-118">Especifica um nome do locatário.</span><span class="sxs-lookup"><span data-stu-id="98ec1-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="98ec1-119">Este cmdlet define a política de teste para o locatário especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="98ec1-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="98ec1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98ec1-120">-PassThru</span></span>
<span data-ttu-id="98ec1-121">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="98ec1-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="98ec1-122">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="98ec1-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="98ec1-123">-Política</span><span class="sxs-lookup"><span data-stu-id="98ec1-123">-Policy</span></span>
<span data-ttu-id="98ec1-124">Especifica o documento de política a ser definido.</span><span class="sxs-lookup"><span data-stu-id="98ec1-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="98ec1-125">O formato da política pode ser Text ou JSON Web Token (JWT).</span><span class="sxs-lookup"><span data-stu-id="98ec1-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="98ec1-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="98ec1-126">-PolicyFormat</span></span>
<span data-ttu-id="98ec1-127">Especifica o formato da política, Text ou JWT (JSON Web Token).</span><span class="sxs-lookup"><span data-stu-id="98ec1-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="98ec1-128">O formato de política padrão é Texto.</span><span class="sxs-lookup"><span data-stu-id="98ec1-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="98ec1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98ec1-129">-ResourceGroupName</span></span>
<span data-ttu-id="98ec1-130">Especifica o nome do grupo de recursos de um provedor de teste.</span><span class="sxs-lookup"><span data-stu-id="98ec1-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="98ec1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98ec1-131">-ResourceId</span></span>
<span data-ttu-id="98ec1-132">Especifica a ResourceID de um provedor de teste.</span><span class="sxs-lookup"><span data-stu-id="98ec1-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="98ec1-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="98ec1-133">-Tee</span></span>
<span data-ttu-id="98ec1-134">Especifica um tipo de Ambiente de Execução Confiável.</span><span class="sxs-lookup"><span data-stu-id="98ec1-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="98ec1-135">Há suporte para quatro tipos de ambiente: SgxEntronice, OpenEn ltda, CyResComponent e VBSEn ltda.</span><span class="sxs-lookup"><span data-stu-id="98ec1-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="98ec1-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="98ec1-136">-Confirm</span></span>
<span data-ttu-id="98ec1-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98ec1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98ec1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98ec1-138">-WhatIf</span></span>
<span data-ttu-id="98ec1-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="98ec1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98ec1-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98ec1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98ec1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ec1-141">CommonParameters</span></span>
<span data-ttu-id="98ec1-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98ec1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ec1-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98ec1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ec1-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="98ec1-144">INPUTS</span></span>

### <span data-ttu-id="98ec1-145">System.String</span><span class="sxs-lookup"><span data-stu-id="98ec1-145">System.String</span></span>

## <span data-ttu-id="98ec1-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="98ec1-146">OUTPUTS</span></span>

### <span data-ttu-id="98ec1-147">System.String</span><span class="sxs-lookup"><span data-stu-id="98ec1-147">System.String</span></span>

## <span data-ttu-id="98ec1-148">Notas</span><span class="sxs-lookup"><span data-stu-id="98ec1-148">NOTES</span></span>

## <span data-ttu-id="98ec1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98ec1-149">RELATED LINKS</span></span>
