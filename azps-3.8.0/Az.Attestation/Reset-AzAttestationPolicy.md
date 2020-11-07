---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: a2b8d83254c84ee974173611912dd9b21cb7a26d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942726"
---
# <span data-ttu-id="f5eab-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="f5eab-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="f5eab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5eab-102">SYNOPSIS</span></span>
<span data-ttu-id="f5eab-103">Redefine a política de um locatário no Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="f5eab-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="f5eab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5eab-104">SYNTAX</span></span>

### <span data-ttu-id="f5eab-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5eab-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5eab-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5eab-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5eab-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5eab-107">DESCRIPTION</span></span>
<span data-ttu-id="f5eab-108">O cmdlet Reset-AzAttestationPolicy redefine a política de atestado definida pelo usuário de um locatário no atestado do Azure.</span><span class="sxs-lookup"><span data-stu-id="f5eab-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f5eab-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5eab-109">EXAMPLES</span></span>

### <span data-ttu-id="f5eab-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f5eab-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="f5eab-111">Redefina a política para o padrão para o provedor de atestado *pshtest* para o tipo de *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="f5eab-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="f5eab-112">OS</span><span class="sxs-lookup"><span data-stu-id="f5eab-112">PARAMETERS</span></span>

### <span data-ttu-id="f5eab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5eab-113">-DefaultProfile</span></span>
<span data-ttu-id="f5eab-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5eab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5eab-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5eab-115">-Name</span></span>
<span data-ttu-id="f5eab-116">Especifica um nome do locatário.</span><span class="sxs-lookup"><span data-stu-id="f5eab-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="f5eab-117">Este cmdlet redefine a política de atestado para o locatário que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f5eab-117">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5eab-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5eab-118">-PassThru</span></span>
<span data-ttu-id="f5eab-119">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="f5eab-119">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f5eab-120">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f5eab-120">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f5eab-121">-Política</span><span class="sxs-lookup"><span data-stu-id="f5eab-121">-Policy</span></span>
<span data-ttu-id="f5eab-122">Especifica o token da Web JSON que descreve o documento de política a ser redefinido.</span><span class="sxs-lookup"><span data-stu-id="f5eab-122">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="f5eab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5eab-123">-ResourceGroupName</span></span>
<span data-ttu-id="f5eab-124">Especifica o nome do grupo de recursos de um provedor de atestado.</span><span class="sxs-lookup"><span data-stu-id="f5eab-124">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="f5eab-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5eab-125">-ResourceId</span></span>
<span data-ttu-id="f5eab-126">Especifica o ResourceId de um provedor de atestado.</span><span class="sxs-lookup"><span data-stu-id="f5eab-126">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="f5eab-127">-T</span><span class="sxs-lookup"><span data-stu-id="f5eab-127">-Tee</span></span>
<span data-ttu-id="f5eab-128">Especifica um tipo de ambiente de execução confiável.</span><span class="sxs-lookup"><span data-stu-id="f5eab-128">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="f5eab-129">Oferecemos suporte a quatro tipos de ambiente: SgxEnclave, OpenEnclave, CyResComponent e VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="f5eab-129">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="f5eab-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5eab-130">-Confirm</span></span>
<span data-ttu-id="f5eab-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5eab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5eab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5eab-132">-WhatIf</span></span>
<span data-ttu-id="f5eab-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5eab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5eab-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5eab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5eab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5eab-135">CommonParameters</span></span>
<span data-ttu-id="f5eab-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5eab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5eab-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5eab-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5eab-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5eab-138">INPUTS</span></span>

### <span data-ttu-id="f5eab-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f5eab-139">System.String</span></span>

## <span data-ttu-id="f5eab-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5eab-140">OUTPUTS</span></span>

### <span data-ttu-id="f5eab-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5eab-141">System.Boolean</span></span>

## <span data-ttu-id="f5eab-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5eab-142">NOTES</span></span>

## <span data-ttu-id="f5eab-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5eab-143">RELATED LINKS</span></span>
