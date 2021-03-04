---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: 54fdbcfe83dd93101030d92f9f3eec19d1a2564f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889513"
---
# <span data-ttu-id="a7c01-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="a7c01-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="a7c01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7c01-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c01-103">Crie ou atualize os metadados de um DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a7c01-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="a7c01-104">O padrão comum para modificar uma propriedade é recuperar os metadados digitalTwinsInstance e segurança e combiná-los com os valores modificados em um novo corpo para atualizar o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a7c01-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="a7c01-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a7c01-105">SYNTAX</span></span>

### <span data-ttu-id="a7c01-106">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="a7c01-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a7c01-107">Criar</span><span class="sxs-lookup"><span data-stu-id="a7c01-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a7c01-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a7c01-108">DESCRIPTION</span></span>
<span data-ttu-id="a7c01-109">Crie ou atualize os metadados de um DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a7c01-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="a7c01-110">O padrão comum para modificar uma propriedade é recuperar os metadados digitalTwinsInstance e segurança e combiná-los com os valores modificados em um novo corpo para atualizar o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a7c01-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="a7c01-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7c01-111">EXAMPLES</span></span>

### <span data-ttu-id="a7c01-112">Exemplo 1: Criar um AzDigitalTwinsInstance por padrão.</span><span class="sxs-lookup"><span data-stu-id="a7c01-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="a7c01-113">Criar um AzDigitalTwinsInstance por padrão</span><span class="sxs-lookup"><span data-stu-id="a7c01-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="a7c01-114">Exemplo 2: Criar um objeto AzDigitalTwinsInstance pelo objeto AzDigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="a7c01-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="a7c01-115">Criar um objeto AzDigitalTwinsInstance by AzDigitalTwins</span><span class="sxs-lookup"><span data-stu-id="a7c01-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="a7c01-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a7c01-116">PARAMETERS</span></span>

### <span data-ttu-id="a7c01-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7c01-117">-AsJob</span></span>
<span data-ttu-id="a7c01-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a7c01-118">Run the command as a job</span></span>

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

### <span data-ttu-id="a7c01-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7c01-119">-DefaultProfile</span></span>
<span data-ttu-id="a7c01-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7c01-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c01-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="a7c01-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="a7c01-122">A descrição do serviço DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="a7c01-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="a7c01-123">Para construir, consulte a seção NOTES para propriedades DIGITALTWINSCREATE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a7c01-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c01-124">-Location</span><span class="sxs-lookup"><span data-stu-id="a7c01-124">-Location</span></span>
<span data-ttu-id="a7c01-125">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="a7c01-125">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c01-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a7c01-126">-NoWait</span></span>
<span data-ttu-id="a7c01-127">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="a7c01-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a7c01-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7c01-128">-ResourceGroupName</span></span>
<span data-ttu-id="a7c01-129">O nome do grupo de recursos que contém DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a7c01-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="a7c01-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a7c01-130">-ResourceName</span></span>
<span data-ttu-id="a7c01-131">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a7c01-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="a7c01-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7c01-132">-SubscriptionId</span></span>
<span data-ttu-id="a7c01-133">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a7c01-133">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c01-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7c01-134">-Tag</span></span>
<span data-ttu-id="a7c01-135">As marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="a7c01-135">The resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c01-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7c01-136">-Confirm</span></span>
<span data-ttu-id="a7c01-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7c01-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7c01-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7c01-138">-WhatIf</span></span>
<span data-ttu-id="a7c01-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7c01-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7c01-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7c01-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7c01-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c01-141">CommonParameters</span></span>
<span data-ttu-id="a7c01-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7c01-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c01-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7c01-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c01-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7c01-144">INPUTS</span></span>

### <span data-ttu-id="a7c01-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="a7c01-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="a7c01-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a7c01-146">OUTPUTS</span></span>

### <span data-ttu-id="a7c01-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="a7c01-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="a7c01-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="a7c01-148">NOTES</span></span>

<span data-ttu-id="a7c01-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a7c01-149">ALIASES</span></span>

<span data-ttu-id="a7c01-150">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="a7c01-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7c01-151">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a7c01-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7c01-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7c01-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7c01-153">DIGITALTWINSCREATE <IDigitalTwinsDescription> : A descrição do serviço DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="a7c01-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="a7c01-154">`Location <String>`: O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="a7c01-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="a7c01-155">`[Tag <IDigitalTwinsResourceTags>]`: As marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="a7c01-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="a7c01-156">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="a7c01-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="a7c01-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7c01-157">RELATED LINKS</span></span>

