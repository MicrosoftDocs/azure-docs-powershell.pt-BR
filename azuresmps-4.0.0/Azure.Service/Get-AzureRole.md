---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946314"
---
# <span data-ttu-id="6265b-101">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="6265b-101">Get-AzureRole</span></span>

## <span data-ttu-id="6265b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6265b-102">SYNOPSIS</span></span>
<span data-ttu-id="6265b-103">Retorna uma lista de funções no seu serviço do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6265b-103">Returns a list of roles in your Microsoft Azure service.</span></span>

## <span data-ttu-id="6265b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6265b-104">SYNTAX</span></span>

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="6265b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6265b-105">DESCRIPTION</span></span>
<span data-ttu-id="6265b-106">O cmdlet **Get-AzureRole** retorna um objeto List com detalhes sobre as funções em seu serviço do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6265b-106">The **Get-AzureRole** cmdlet returns a list object with details on the roles in your Microsoft Azure service.</span></span>
<span data-ttu-id="6265b-107">Se você especificar o parâmetro *roleName* , **Get-AzureRole** retornará detalhes sobre essa função apenas.</span><span class="sxs-lookup"><span data-stu-id="6265b-107">If you specify the *RoleName* parameter, **Get-AzureRole** returns details on that role only.</span></span>
<span data-ttu-id="6265b-108">Se você especificar o parâmetro *InstanceDetails* , detalhes adicionais específicos da instância serão retornados.</span><span class="sxs-lookup"><span data-stu-id="6265b-108">If you specify the *InstanceDetails* parameter, additional, instance-specific details are returned.</span></span>

## <span data-ttu-id="6265b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6265b-109">EXAMPLES</span></span>

### <span data-ttu-id="6265b-110">Exemplo 1: obter uma lista de funções para um serviço</span><span class="sxs-lookup"><span data-stu-id="6265b-110">Example 1: Get a list of roles for a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

<span data-ttu-id="6265b-111">Esse comando retorna um objeto com detalhes sobre todas as funções de produção em execução no serviço MySvc01.</span><span class="sxs-lookup"><span data-stu-id="6265b-111">This command returns an object with details on all the production roles running on the MySvc01 service.</span></span>

### <span data-ttu-id="6265b-112">Exemplo 2: obter detalhes sobre uma função em execução em um serviço</span><span class="sxs-lookup"><span data-stu-id="6265b-112">Example 2: Get details on a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

<span data-ttu-id="6265b-113">Esse comando retorna um objeto com detalhes na função MyTestVM3, em execução no ambiente de preparo do serviço MySvc01.</span><span class="sxs-lookup"><span data-stu-id="6265b-113">This command returns an object with details on the MyTestVM3 role, running on the staging environment of the MySvc01 service.</span></span>

### <span data-ttu-id="6265b-114">Exemplo 3: obter informações de instância sobre instâncias de uma função em execução em um serviço</span><span class="sxs-lookup"><span data-stu-id="6265b-114">Example 3: Get instance information on instances of a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

<span data-ttu-id="6265b-115">Esse comando retorna um objeto com detalhes nas instâncias da função MyTestVM02 em execução no ambiente de produção do serviço MySvc01.</span><span class="sxs-lookup"><span data-stu-id="6265b-115">This command returns an object with details on the instances of the MyTestVM02 role running in the production environment on the MySvc01 service.</span></span>

### <span data-ttu-id="6265b-116">Exemplo 4: obter uma tabela das instâncias de função associadas a um serviço</span><span class="sxs-lookup"><span data-stu-id="6265b-116">Example 4: Get a table of the role instances associated with a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

<span data-ttu-id="6265b-117">Esse comando retorna uma tabela do nome da instância, tamanho e status de todas as instâncias de função em execução no ambiente de produção no serviço MySvc01.</span><span class="sxs-lookup"><span data-stu-id="6265b-117">This command returns a table of the instance name, size, and status of all role instances running in the production environment on the MySvc01 service.</span></span>

## <span data-ttu-id="6265b-118">OS</span><span class="sxs-lookup"><span data-stu-id="6265b-118">PARAMETERS</span></span>

### <span data-ttu-id="6265b-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="6265b-119">-InformationAction</span></span>
<span data-ttu-id="6265b-120">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="6265b-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6265b-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6265b-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6265b-122">Contínuo</span><span class="sxs-lookup"><span data-stu-id="6265b-122">Continue</span></span>
- <span data-ttu-id="6265b-123">Ignorar</span><span class="sxs-lookup"><span data-stu-id="6265b-123">Ignore</span></span>
- <span data-ttu-id="6265b-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="6265b-124">Inquire</span></span>
- <span data-ttu-id="6265b-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6265b-125">SilentlyContinue</span></span>
- <span data-ttu-id="6265b-126">Finaliza</span><span class="sxs-lookup"><span data-stu-id="6265b-126">Stop</span></span>
- <span data-ttu-id="6265b-127">Suspensão</span><span class="sxs-lookup"><span data-stu-id="6265b-127">Suspend</span></span>

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

### <span data-ttu-id="6265b-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6265b-128">-InformationVariable</span></span>
<span data-ttu-id="6265b-129">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="6265b-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6265b-130">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="6265b-130">-InstanceDetails</span></span>
<span data-ttu-id="6265b-131">Especifica que esse cmdlet retorna detalhes sobre as instâncias em cada função.</span><span class="sxs-lookup"><span data-stu-id="6265b-131">Specifies that this cmdlet returns details about the instances on each role.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6265b-132">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6265b-132">-Profile</span></span>
<span data-ttu-id="6265b-133">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6265b-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6265b-134">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6265b-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6265b-135">-RoleName</span><span class="sxs-lookup"><span data-stu-id="6265b-135">-RoleName</span></span>
<span data-ttu-id="6265b-136">Especifica o nome da função a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="6265b-136">Specifies the name of the role to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6265b-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6265b-137">-ServiceName</span></span>
<span data-ttu-id="6265b-138">Especifica o nome do serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="6265b-138">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="6265b-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="6265b-139">-Slot</span></span>
<span data-ttu-id="6265b-140">Especifica o ambiente de implantação do Azure.</span><span class="sxs-lookup"><span data-stu-id="6265b-140">Specifies the Azure deployment environment.</span></span>
<span data-ttu-id="6265b-141">Os valores aceitáveis para esse parâmetro são: produção ou preparação.</span><span class="sxs-lookup"><span data-stu-id="6265b-141">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6265b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6265b-142">CommonParameters</span></span>
<span data-ttu-id="6265b-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6265b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6265b-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6265b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6265b-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6265b-145">INPUTS</span></span>

## <span data-ttu-id="6265b-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6265b-146">OUTPUTS</span></span>

## <span data-ttu-id="6265b-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6265b-147">NOTES</span></span>

## <span data-ttu-id="6265b-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6265b-148">RELATED LINKS</span></span>

[<span data-ttu-id="6265b-149">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="6265b-149">Set-AzureRole</span></span>](./Set-AzureRole.md)


