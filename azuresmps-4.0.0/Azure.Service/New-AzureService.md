---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BB216903-B2BB-4948-AC28-408ED6C768F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6cae249f99282006ff8636e8d727485a223e2a1d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945899"
---
# <span data-ttu-id="1ee8a-101">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="1ee8a-101">New-AzureService</span></span>

## <span data-ttu-id="1ee8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ee8a-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee8a-103">Cria um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-103">Creates an Azure service.</span></span>

## <span data-ttu-id="1ee8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ee8a-104">SYNTAX</span></span>

### <span data-ttu-id="1ee8a-105">ParameterSetAffinityGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ee8a-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureService [-ServiceName] <String> [-AffinityGroup] <String> [[-Label] <String>]
 [[-Description] <String>] [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1ee8a-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="1ee8a-106">ParameterSetLocation</span></span>
```
New-AzureService [-ServiceName] <String> [-Location] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1ee8a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ee8a-107">DESCRIPTION</span></span>
<span data-ttu-id="1ee8a-108">O cmdlet **New-AzureService** cria um novo serviço do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-108">The **New-AzureService** cmdlet creates a new Azure service in the current subscription.</span></span>

## <span data-ttu-id="1ee8a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ee8a-109">EXAMPLES</span></span>

### <span data-ttu-id="1ee8a-110">Exemplo 1: criar um serviço</span><span class="sxs-lookup"><span data-stu-id="1ee8a-110">Example 1: Create a service</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -Label "MyTestService" -Location "South Central US"
```

<span data-ttu-id="1ee8a-111">Esse comando cria um novo serviço chamado MySvc01 no local central do Sul dos EUA.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-111">This command creates a new service named MySvc01 in the South Central US location.</span></span>

### <span data-ttu-id="1ee8a-112">Exemplo 2: criar um serviço em um grupo de afinidade</span><span class="sxs-lookup"><span data-stu-id="1ee8a-112">Example 2: Create a service in an affinity group</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -AffinityGroup NorthRegion
```

<span data-ttu-id="1ee8a-113">Esse comando cria um novo serviço chamado MySvc01 usando o grupo de afinidade do NorthRegion.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-113">This command creates a new service named MySvc01 using the NorthRegion affinity group.</span></span>

## <span data-ttu-id="1ee8a-114">OS</span><span class="sxs-lookup"><span data-stu-id="1ee8a-114">PARAMETERS</span></span>

### <span data-ttu-id="1ee8a-115">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="1ee8a-115">-AffinityGroup</span></span>
<span data-ttu-id="1ee8a-116">Especifica o grupo de afinidade associado à assinatura.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-116">Specifies the affinity group associated with the subscription.</span></span>
<span data-ttu-id="1ee8a-117">Se você não especificar o parâmetro *Location* , será necessário um grupo Affinity.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-117">If you do not specify the *Location* parameter, an affinity group is required.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee8a-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="1ee8a-118">-Description</span></span>
<span data-ttu-id="1ee8a-119">Especifica uma descrição para o serviço.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-119">Specifies a description for the service.</span></span>
<span data-ttu-id="1ee8a-120">A descrição pode ter até 1024 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-120">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee8a-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="1ee8a-121">-InformationAction</span></span>
<span data-ttu-id="1ee8a-122">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1ee8a-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1ee8a-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1ee8a-124">Contínuo</span><span class="sxs-lookup"><span data-stu-id="1ee8a-124">Continue</span></span>
- <span data-ttu-id="1ee8a-125">Ignorar</span><span class="sxs-lookup"><span data-stu-id="1ee8a-125">Ignore</span></span>
- <span data-ttu-id="1ee8a-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="1ee8a-126">Inquire</span></span>
- <span data-ttu-id="1ee8a-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1ee8a-127">SilentlyContinue</span></span>
- <span data-ttu-id="1ee8a-128">Finaliza</span><span class="sxs-lookup"><span data-stu-id="1ee8a-128">Stop</span></span>
- <span data-ttu-id="1ee8a-129">Suspensão</span><span class="sxs-lookup"><span data-stu-id="1ee8a-129">Suspend</span></span>

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

### <span data-ttu-id="1ee8a-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1ee8a-130">-InformationVariable</span></span>
<span data-ttu-id="1ee8a-131">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1ee8a-132">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="1ee8a-132">-Label</span></span>
<span data-ttu-id="1ee8a-133">Especifica um rótulo para o serviço.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-133">Specifies a label for the service.</span></span>
<span data-ttu-id="1ee8a-134">O rótulo pode ter até 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-134">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee8a-135">-Local</span><span class="sxs-lookup"><span data-stu-id="1ee8a-135">-Location</span></span>
<span data-ttu-id="1ee8a-136">Especifica o local do serviço.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-136">Specifies the location for the service.</span></span>
<span data-ttu-id="1ee8a-137">Um local será necessário se não houver um grupo de afinidade especificado.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-137">A location is required if there isn't a specified Affinity Group.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee8a-138">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1ee8a-138">-Profile</span></span>
<span data-ttu-id="1ee8a-139">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ee8a-140">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ee8a-141">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="1ee8a-141">-ReverseDnsFqdn</span></span>
<span data-ttu-id="1ee8a-142">Especifica o nome de domínio totalmente qualificado para DNS reverso.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-142">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee8a-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1ee8a-143">-ServiceName</span></span>
<span data-ttu-id="1ee8a-144">Especifica o nome do novo serviço.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-144">Specifies the name of the new service.</span></span>
<span data-ttu-id="1ee8a-145">O nome deve ser exclusivo para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-145">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="1ee8a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee8a-146">CommonParameters</span></span>
<span data-ttu-id="1ee8a-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee8a-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee8a-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee8a-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ee8a-149">INPUTS</span></span>

## <span data-ttu-id="1ee8a-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ee8a-150">OUTPUTS</span></span>

## <span data-ttu-id="1ee8a-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ee8a-151">NOTES</span></span>

## <span data-ttu-id="1ee8a-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ee8a-152">RELATED LINKS</span></span>

[<span data-ttu-id="1ee8a-153">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="1ee8a-153">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="1ee8a-154">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="1ee8a-154">Set-AzureService</span></span>](./Set-AzureService.md)


