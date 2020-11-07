---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945952"
---
# <span data-ttu-id="b850b-101">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="b850b-101">Set-AzureServiceProjectRole</span></span>

## <span data-ttu-id="b850b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b850b-102">SYNOPSIS</span></span>
<span data-ttu-id="b850b-103">Define o número de instâncias ou a versão de tempo de execução de uma função.</span><span class="sxs-lookup"><span data-stu-id="b850b-103">Sets the number of instances or the runtime version of a role.</span></span>

## <span data-ttu-id="b850b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b850b-104">SYNTAX</span></span>

### <span data-ttu-id="b850b-105">Instância</span><span class="sxs-lookup"><span data-stu-id="b850b-105">Instances</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="b850b-106">Classpath</span><span class="sxs-lookup"><span data-stu-id="b850b-106">Runtime</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b850b-107">VMSize</span><span class="sxs-lookup"><span data-stu-id="b850b-107">VMSize</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b850b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b850b-108">DESCRIPTION</span></span>
<span data-ttu-id="b850b-109">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b850b-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b850b-110">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b850b-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b850b-111">O cmdlet **set-AzureServiceProjectRole** define o número de instâncias de função para a função especificada.</span><span class="sxs-lookup"><span data-stu-id="b850b-111">The **Set-AzureServiceProjectRole** cmdlet sets the number of role instances for the specified role.</span></span>

## <span data-ttu-id="b850b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b850b-112">EXAMPLES</span></span>

### <span data-ttu-id="b850b-113">Exemplo 1: definir instâncias para uma função da Web</span><span class="sxs-lookup"><span data-stu-id="b850b-113">Example 1: Set instances for a web role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

<span data-ttu-id="b850b-114">Define o número de instâncias para a função da Web chamada MyWebRole1 para 2.</span><span class="sxs-lookup"><span data-stu-id="b850b-114">Sets the number of instances for the web role named MyWebRole1 to 2.</span></span>

### <span data-ttu-id="b850b-115">Exemplo 2: definir instâncias para uma função de trabalhador</span><span class="sxs-lookup"><span data-stu-id="b850b-115">Example 2: Set instances for a worker role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

<span data-ttu-id="b850b-116">Define a contagem de instâncias de função para a função de trabalho chamada WorkerRole1 para 2.</span><span class="sxs-lookup"><span data-stu-id="b850b-116">Sets the role instance count for the worker role named WorkerRole1 to 2.</span></span>

### <span data-ttu-id="b850b-117">Exemplo 3: definir a versão do tempo de execução para um serviço de função</span><span class="sxs-lookup"><span data-stu-id="b850b-117">Example 3: Set the runtime version for a role service</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

<span data-ttu-id="b850b-118">Define a versão do node.exe Runtime para a função MyRole1 como 0.6.20.</span><span class="sxs-lookup"><span data-stu-id="b850b-118">Sets the node.exe runtime version for role MyRole1 to 0.6.20.</span></span>

## <span data-ttu-id="b850b-119">OS</span><span class="sxs-lookup"><span data-stu-id="b850b-119">PARAMETERS</span></span>

### <span data-ttu-id="b850b-120">-Instâncias</span><span class="sxs-lookup"><span data-stu-id="b850b-120">-Instances</span></span>
<span data-ttu-id="b850b-121">Especifica o número de instâncias de função para a função de trabalho ou da Web especificada.</span><span class="sxs-lookup"><span data-stu-id="b850b-121">Specifies the number of role instances for the specified web or worker role.</span></span>

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b850b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b850b-122">-PassThru</span></span>
<span data-ttu-id="b850b-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b850b-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b850b-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b850b-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b850b-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b850b-125">-Profile</span></span>
<span data-ttu-id="b850b-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b850b-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b850b-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b850b-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b850b-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="b850b-128">-RoleName</span></span>
<span data-ttu-id="b850b-129">Especifica o nome da função de trabalho ou Web a ser alterada.</span><span class="sxs-lookup"><span data-stu-id="b850b-129">Specifies the name of the web or worker role to be changed.</span></span>

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

### <span data-ttu-id="b850b-130">-Runtime</span><span class="sxs-lookup"><span data-stu-id="b850b-130">-Runtime</span></span>
<span data-ttu-id="b850b-131">Especifica o tempo de execução para adicionar à função especificada.</span><span class="sxs-lookup"><span data-stu-id="b850b-131">Specifies the runtime to add to the specified role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b850b-132">-Versão</span><span class="sxs-lookup"><span data-stu-id="b850b-132">-Version</span></span>
<span data-ttu-id="b850b-133">Especifica a versão do tempo de execução para adicionar à função.</span><span class="sxs-lookup"><span data-stu-id="b850b-133">Specifies the version of the runtime to add to the role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b850b-134">-VMSize</span><span class="sxs-lookup"><span data-stu-id="b850b-134">-VMSize</span></span>
<span data-ttu-id="b850b-135">Especifica o tamanho da máquina virtual da função.</span><span class="sxs-lookup"><span data-stu-id="b850b-135">Specifies the virtual machine size of the role.</span></span>

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b850b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b850b-136">CommonParameters</span></span>
<span data-ttu-id="b850b-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b850b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b850b-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b850b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b850b-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b850b-139">INPUTS</span></span>

###  
<span data-ttu-id="b850b-140">Especifica o tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b850b-140">Specifies the size of the virtual machine.</span></span>

## <span data-ttu-id="b850b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b850b-141">OUTPUTS</span></span>

## <span data-ttu-id="b850b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b850b-142">NOTES</span></span>

## <span data-ttu-id="b850b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b850b-143">RELATED LINKS</span></span>

[<span data-ttu-id="b850b-144">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="b850b-144">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


