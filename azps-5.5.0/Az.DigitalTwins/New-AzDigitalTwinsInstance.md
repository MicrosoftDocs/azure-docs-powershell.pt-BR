---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: d6a748897b956759ad64056b0d9b83a6e82e91fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116812"
---
# <span data-ttu-id="48330-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="48330-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="48330-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48330-102">SYNOPSIS</span></span>
<span data-ttu-id="48330-103">Criar ou atualizar os metadados de uma DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="48330-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="48330-104">O padrão normal para modificar uma propriedade é recuperar os metadados de segurança e DigitalTwinsInstance e combiná-los com os valores modificados em um novo corpo para atualizar o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="48330-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="48330-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48330-105">SYNTAX</span></span>

### <span data-ttu-id="48330-106">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="48330-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="48330-107">Criar</span><span class="sxs-lookup"><span data-stu-id="48330-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="48330-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="48330-108">DESCRIPTION</span></span>
<span data-ttu-id="48330-109">Criar ou atualizar os metadados de uma DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="48330-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="48330-110">O padrão normal para modificar uma propriedade é recuperar os metadados de segurança e DigitalTwinsInstance e combiná-los com os valores modificados em um novo corpo para atualizar o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="48330-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="48330-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48330-111">EXAMPLES</span></span>

### <span data-ttu-id="48330-112">Exemplo 1: Criar um AzDigitalTwinsInstance por padrão.</span><span class="sxs-lookup"><span data-stu-id="48330-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="48330-113">Criar um AzDigitalTwinsInstance por padrão</span><span class="sxs-lookup"><span data-stu-id="48330-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="48330-114">Exemplo 2: Criar um Objeto AzDigitalTwinsInstance por AzDigitalTwins Object.</span><span class="sxs-lookup"><span data-stu-id="48330-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="48330-115">Criar um objeto AzDigitalTwinsInstance por AzDigitalTwins Object</span><span class="sxs-lookup"><span data-stu-id="48330-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="48330-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48330-116">PARAMETERS</span></span>

### <span data-ttu-id="48330-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48330-117">-AsJob</span></span>
<span data-ttu-id="48330-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="48330-118">Run the command as a job</span></span>

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

### <span data-ttu-id="48330-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48330-119">-DefaultProfile</span></span>
<span data-ttu-id="48330-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48330-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48330-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="48330-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="48330-122">A descrição do serviço DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="48330-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="48330-123">Para construir, confira a seção ANOTAÇÕES para propriedades DIGITALTWINSCREATE e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="48330-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="48330-124">-Local</span><span class="sxs-lookup"><span data-stu-id="48330-124">-Location</span></span>
<span data-ttu-id="48330-125">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="48330-125">The resource location.</span></span>

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

### <span data-ttu-id="48330-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="48330-126">-NoWait</span></span>
<span data-ttu-id="48330-127">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="48330-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="48330-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48330-128">-ResourceGroupName</span></span>
<span data-ttu-id="48330-129">O nome do grupo de recursos que contém a DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="48330-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="48330-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="48330-130">-ResourceName</span></span>
<span data-ttu-id="48330-131">O nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="48330-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="48330-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48330-132">-SubscriptionId</span></span>
<span data-ttu-id="48330-133">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="48330-133">The subscription identifier.</span></span>

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

### <span data-ttu-id="48330-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="48330-134">-Tag</span></span>
<span data-ttu-id="48330-135">As marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="48330-135">The resource tags.</span></span>

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

### <span data-ttu-id="48330-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="48330-136">-Confirm</span></span>
<span data-ttu-id="48330-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48330-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48330-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48330-138">-WhatIf</span></span>
<span data-ttu-id="48330-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="48330-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48330-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48330-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48330-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48330-141">CommonParameters</span></span>
<span data-ttu-id="48330-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48330-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48330-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48330-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48330-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="48330-144">INPUTS</span></span>

### <span data-ttu-id="48330-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="48330-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="48330-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="48330-146">OUTPUTS</span></span>

### <span data-ttu-id="48330-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="48330-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="48330-148">Notas</span><span class="sxs-lookup"><span data-stu-id="48330-148">NOTES</span></span>

<span data-ttu-id="48330-149">Aliases</span><span class="sxs-lookup"><span data-stu-id="48330-149">ALIASES</span></span>

<span data-ttu-id="48330-150">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="48330-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48330-151">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="48330-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48330-152">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="48330-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48330-153">DIGITALTWINSCREATE: <IDigitalTwinsDescription> a descrição do serviço DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="48330-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="48330-154">`Location <String>`: o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="48330-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="48330-155">`[Tag <IDigitalTwinsResourceTags>]`: as marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="48330-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="48330-156">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="48330-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="48330-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48330-157">RELATED LINKS</span></span>

