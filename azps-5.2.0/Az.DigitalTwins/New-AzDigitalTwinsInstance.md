---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: d6a748897b956759ad64056b0d9b83a6e82e91fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260544"
---
# <span data-ttu-id="b65c1-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="b65c1-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="b65c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b65c1-102">SYNOPSIS</span></span>
<span data-ttu-id="b65c1-103">Criar ou atualizar os metadados de um DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b65c1-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="b65c1-104">O padrão usual para modificar uma propriedade é recuperar os metadados DigitalTwinsInstance e Security e, em seguida, combiná-los com os valores modificados em um novo corpo para atualizar o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b65c1-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="b65c1-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b65c1-105">SYNTAX</span></span>

### <span data-ttu-id="b65c1-106">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="b65c1-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b65c1-107">Criados</span><span class="sxs-lookup"><span data-stu-id="b65c1-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b65c1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b65c1-108">DESCRIPTION</span></span>
<span data-ttu-id="b65c1-109">Criar ou atualizar os metadados de um DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b65c1-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="b65c1-110">O padrão usual para modificar uma propriedade é recuperar os metadados DigitalTwinsInstance e Security e, em seguida, combiná-los com os valores modificados em um novo corpo para atualizar o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b65c1-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="b65c1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b65c1-111">EXAMPLES</span></span>

### <span data-ttu-id="b65c1-112">Exemplo 1: criar um AzDigitalTwinsInstance por padrão.</span><span class="sxs-lookup"><span data-stu-id="b65c1-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b65c1-113">Criar um AzDigitalTwinsInstance por padrão</span><span class="sxs-lookup"><span data-stu-id="b65c1-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="b65c1-114">Exemplo 2: criar um AzDigitalTwinsInstance por objeto AzDigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="b65c1-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b65c1-115">Criar um AzDigitalTwinsInstance por objeto AzDigitalTwins</span><span class="sxs-lookup"><span data-stu-id="b65c1-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="b65c1-116">OS</span><span class="sxs-lookup"><span data-stu-id="b65c1-116">PARAMETERS</span></span>

### <span data-ttu-id="b65c1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b65c1-117">-AsJob</span></span>
<span data-ttu-id="b65c1-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="b65c1-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b65c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65c1-119">-DefaultProfile</span></span>
<span data-ttu-id="b65c1-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b65c1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b65c1-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="b65c1-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="b65c1-122">A descrição do serviço DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="b65c1-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="b65c1-123">Para construir, consulte a seção notas para propriedades DIGITALTWINSCREATE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b65c1-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="b65c1-124">-Local</span><span class="sxs-lookup"><span data-stu-id="b65c1-124">-Location</span></span>
<span data-ttu-id="b65c1-125">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b65c1-125">The resource location.</span></span>

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

### <span data-ttu-id="b65c1-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b65c1-126">-NoWait</span></span>
<span data-ttu-id="b65c1-127">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="b65c1-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b65c1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b65c1-128">-ResourceGroupName</span></span>
<span data-ttu-id="b65c1-129">O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b65c1-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="b65c1-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b65c1-130">-ResourceName</span></span>
<span data-ttu-id="b65c1-131">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b65c1-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="b65c1-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b65c1-132">-SubscriptionId</span></span>
<span data-ttu-id="b65c1-133">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="b65c1-133">The subscription identifier.</span></span>

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

### <span data-ttu-id="b65c1-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="b65c1-134">-Tag</span></span>
<span data-ttu-id="b65c1-135">As marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="b65c1-135">The resource tags.</span></span>

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

### <span data-ttu-id="b65c1-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b65c1-136">-Confirm</span></span>
<span data-ttu-id="b65c1-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b65c1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b65c1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b65c1-138">-WhatIf</span></span>
<span data-ttu-id="b65c1-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b65c1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b65c1-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b65c1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b65c1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65c1-141">CommonParameters</span></span>
<span data-ttu-id="b65c1-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b65c1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65c1-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b65c1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65c1-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b65c1-144">INPUTS</span></span>

### <span data-ttu-id="b65c1-145">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="b65c1-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="b65c1-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b65c1-146">OUTPUTS</span></span>

### <span data-ttu-id="b65c1-147">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="b65c1-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="b65c1-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b65c1-148">NOTES</span></span>

<span data-ttu-id="b65c1-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b65c1-149">ALIASES</span></span>

<span data-ttu-id="b65c1-150">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="b65c1-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b65c1-151">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b65c1-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b65c1-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b65c1-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b65c1-153">DIGITALTWINSCREATE <IDigitalTwinsDescription> : a descrição do serviço DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="b65c1-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="b65c1-154">`Location <String>`: O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b65c1-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="b65c1-155">`[Tag <IDigitalTwinsResourceTags>]`: As marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="b65c1-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="b65c1-156">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="b65c1-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="b65c1-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b65c1-157">RELATED LINKS</span></span>

