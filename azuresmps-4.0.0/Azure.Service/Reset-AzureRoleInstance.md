---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945480"
---
# <span data-ttu-id="612b4-101">Reset-AzureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="612b4-101">Reset-AzureRoleInstance</span></span>

## <span data-ttu-id="612b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="612b4-102">SYNOPSIS</span></span>
<span data-ttu-id="612b4-103">Solicita uma reinicialização ou reimagem de uma única instância de função ou de todas as instâncias de função de uma função específica.</span><span class="sxs-lookup"><span data-stu-id="612b4-103">Requests a reboot or reimage of a single role instance or all role instances of a specific role.</span></span>

## <span data-ttu-id="612b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="612b4-104">SYNTAX</span></span>

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="612b4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="612b4-105">DESCRIPTION</span></span>
<span data-ttu-id="612b4-106">O cmdlet **Reset-AzureRoleInstance** solicita uma reinicialização ou uma reimagem de uma instância de função que está sendo executada em uma implantação.</span><span class="sxs-lookup"><span data-stu-id="612b4-106">The **Reset-AzureRoleInstance** cmdlet requests a reboot or a reimage of a role instance that is running in a deployment.</span></span>
<span data-ttu-id="612b4-107">Esta operação é executada sincronicamente.</span><span class="sxs-lookup"><span data-stu-id="612b4-107">This operation executes synchronously.</span></span>
<span data-ttu-id="612b4-108">Quando você reinicializa uma instância de função, o Azure leva a instância offline, reinicia o sistema operacional subjacente para essa instância e coloca a instância novamente online.</span><span class="sxs-lookup"><span data-stu-id="612b4-108">When you reboot a role instance, Azure takes the instance offline, restarts the underlying operating system for that instance, and brings the instance back online.</span></span>
<span data-ttu-id="612b4-109">Todos os dados gravados no disco local persistem nas reinicializações.</span><span class="sxs-lookup"><span data-stu-id="612b4-109">Any data that is written to the local disk persists across reboots.</span></span>
<span data-ttu-id="612b4-110">Todos os dados que estiverem na memória serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="612b4-110">Any data that is in-memory is lost.</span></span>

<span data-ttu-id="612b4-111">A recriação de uma instância de uma instância de função resulta em um comportamento diferente dependendo do tipo de função.</span><span class="sxs-lookup"><span data-stu-id="612b4-111">Reimaging a role instance results in different behavior depending on the type of role.</span></span>
<span data-ttu-id="612b4-112">Para uma função de trabalho ou Web, quando a função é renovada, o Azure leva a função offline e grava uma instalação nova do sistema operacional convidado do Azure para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="612b4-112">For a web or worker role, when the role is reimaged, Azure takes the role offline and writes a fresh installation of the Azure guest operating system to the virtual machine.</span></span>
<span data-ttu-id="612b4-113">A função é então colocada novamente online.</span><span class="sxs-lookup"><span data-stu-id="612b4-113">The role is then brought back online.</span></span>
<span data-ttu-id="612b4-114">Para uma função de VM, quando a função é renovada, o Azure leva a função offline, reaplica a imagem personalizada que você forneceu para ele e coloca a função online novamente.</span><span class="sxs-lookup"><span data-stu-id="612b4-114">For a VM role, when the role is reimaged, Azure takes the role offline, reapplies the custom image that you provided for it, and brings the role back online.</span></span>

<span data-ttu-id="612b4-115">O Azure tenta manter dados em qualquer recurso de armazenamento local quando a função é renovada; no entanto, no caso de uma falha transitória de hardware, o recurso de armazenamento local pode ser perdido.</span><span class="sxs-lookup"><span data-stu-id="612b4-115">Azure attempts to maintain data in any local storage resources when the role is reimaged; however, in case of a transient hardware failure, the local storage resource may be lost.</span></span>
<span data-ttu-id="612b4-116">Se o seu aplicativo requer que os dados persistam, é recomendável gravar em uma fonte de dados durável, como uma unidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="612b4-116">If your application requires that data persist, writing to a durable data source, such as an Azure drive, is recommended.</span></span>
<span data-ttu-id="612b4-117">Todos os dados gravados em um diretório local diferente daquele definido pelo recurso de armazenamento local serão perdidos quando a função for refeita a imagem.</span><span class="sxs-lookup"><span data-stu-id="612b4-117">Any data that is written to a local directory other than that defined by the local storage resource will be lost when the role is reimaged.</span></span>

## <span data-ttu-id="612b4-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="612b4-118">EXAMPLES</span></span>

### <span data-ttu-id="612b4-119">Exemplo 1: reinicie uma instância de função</span><span class="sxs-lookup"><span data-stu-id="612b4-119">Example 1: Reboot a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

<span data-ttu-id="612b4-120">Esse comando reinicializa a instância de função chamada MyWebRole_IN_0 na implantação de preparo do serviço MySvc01.</span><span class="sxs-lookup"><span data-stu-id="612b4-120">This command reboots the role instance named MyWebRole_IN_0 in the staging deployment of the MySvc01 service.</span></span>

### <span data-ttu-id="612b4-121">Exemplo 2: reimagem de uma instância de função</span><span class="sxs-lookup"><span data-stu-id="612b4-121">Example 2: Reimage a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

<span data-ttu-id="612b4-122">Esse comando renovar as instâncias de função na implantação de preparo do serviço de nuvem do MySvc01.</span><span class="sxs-lookup"><span data-stu-id="612b4-122">This command reimages the role instances in the staging deployment of the MySvc01 cloud service.</span></span>

### <span data-ttu-id="612b4-123">Exemplo 3: reimagem de todas as instâncias de função</span><span class="sxs-lookup"><span data-stu-id="612b4-123">Example 3: Reimage all role instances</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

<span data-ttu-id="612b4-124">Esse comando renovar todas as instâncias de função na implantação de produção do serviço MySvc01.</span><span class="sxs-lookup"><span data-stu-id="612b4-124">This command reimages all role instances in the production deployment of the MySvc01 service.</span></span>

## <span data-ttu-id="612b4-125">OS</span><span class="sxs-lookup"><span data-stu-id="612b4-125">PARAMETERS</span></span>

### <span data-ttu-id="612b4-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="612b4-126">-InformationAction</span></span>
<span data-ttu-id="612b4-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="612b4-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="612b4-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="612b4-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="612b4-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="612b4-129">Continue</span></span>
- <span data-ttu-id="612b4-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="612b4-130">Ignore</span></span>
- <span data-ttu-id="612b4-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="612b4-131">Inquire</span></span>
- <span data-ttu-id="612b4-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="612b4-132">SilentlyContinue</span></span>
- <span data-ttu-id="612b4-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="612b4-133">Stop</span></span>
- <span data-ttu-id="612b4-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="612b4-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="612b4-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="612b4-135">-InformationVariable</span></span>
<span data-ttu-id="612b4-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="612b4-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="612b4-137">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="612b4-137">-InstanceName</span></span>
<span data-ttu-id="612b4-138">Especifica o nome da instância de função a ser reinicializada ou reinicializada.</span><span class="sxs-lookup"><span data-stu-id="612b4-138">Specifies the name of the role instance to reimage or reboot.</span></span>

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

### <span data-ttu-id="612b4-139">-Perfil</span><span class="sxs-lookup"><span data-stu-id="612b4-139">-Profile</span></span>
<span data-ttu-id="612b4-140">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="612b4-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="612b4-141">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="612b4-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="612b4-142">-Reboot</span><span class="sxs-lookup"><span data-stu-id="612b4-142">-Reboot</span></span>
<span data-ttu-id="612b4-143">Especifica que esse cmdlet reinicializa a instância de função especificada ou, se nenhuma for especificada, todas as instâncias de função.</span><span class="sxs-lookup"><span data-stu-id="612b4-143">Specifies that this cmdlet reboots the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="612b4-144">Você deve incluir o parâmetro *reboot* ou *Reimage* , mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="612b4-144">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="612b4-145">-Nova imagem</span><span class="sxs-lookup"><span data-stu-id="612b4-145">-Reimage</span></span>
<span data-ttu-id="612b4-146">Especifica que esse cmdlet reimagemia a instância de função especificada ou, se nenhuma for especificada, todas as instâncias de função.</span><span class="sxs-lookup"><span data-stu-id="612b4-146">Specifies that this cmdlet reimages the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="612b4-147">Você deve incluir o parâmetro *reboot* ou *Reimage* , mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="612b4-147">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="612b4-148">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="612b4-148">-ServiceName</span></span>
<span data-ttu-id="612b4-149">Especifica o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="612b4-149">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="612b4-150">-Slot</span><span class="sxs-lookup"><span data-stu-id="612b4-150">-Slot</span></span>
<span data-ttu-id="612b4-151">Especifica o ambiente de implantação onde as instâncias de função são executadas.</span><span class="sxs-lookup"><span data-stu-id="612b4-151">Specifies the deployment environment where the role instances run.</span></span>
<span data-ttu-id="612b4-152">Os valores válidos são: produção e preparação.</span><span class="sxs-lookup"><span data-stu-id="612b4-152">Valid values are: Production and Staging.</span></span>
<span data-ttu-id="612b4-153">Você pode incluir o *deploymentname* ou o parâmetro *slot* , mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="612b4-153">You can include either the *DeploymentName* or *Slot* parameter, but not both.</span></span>

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

### <span data-ttu-id="612b4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="612b4-154">CommonParameters</span></span>
<span data-ttu-id="612b4-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="612b4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="612b4-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="612b4-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="612b4-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="612b4-157">INPUTS</span></span>

## <span data-ttu-id="612b4-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="612b4-158">OUTPUTS</span></span>

## <span data-ttu-id="612b4-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="612b4-159">NOTES</span></span>

## <span data-ttu-id="612b4-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="612b4-160">RELATED LINKS</span></span>

[<span data-ttu-id="612b4-161">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="612b4-161">Set-AzureRole</span></span>](./Set-AzureRole.md)


