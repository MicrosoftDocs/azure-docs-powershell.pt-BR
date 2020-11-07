---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2171943B-D1AC-45FD-99FD-DD0C14AFC60C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38990d3084cf5f494dc811ec6fe458003b8313c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946355"
---
# <span data-ttu-id="6b5f1-101">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6b5f1-101">Get-AzureDeployment</span></span>

## <span data-ttu-id="6b5f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="6b5f1-103">Obtém detalhes de uma implantação.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-103">Gets details of a deployment.</span></span>

## <span data-ttu-id="6b5f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b5f1-104">SYNTAX</span></span>

```
Get-AzureDeployment [-ServiceName] <String> [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6b5f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b5f1-105">DESCRIPTION</span></span>
<span data-ttu-id="6b5f1-106">O cmdlet **Get-AzureDeployment** Obtém detalhes de uma implantação do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-106">The **Get-AzureDeployment** cmdlet gets details of an Azure deployment.</span></span>
<span data-ttu-id="6b5f1-107">Especifique o nome do serviço do Azure e o slot da implantação.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-107">Specify the name of the Azure service and the slot of the deployment.</span></span>

## <span data-ttu-id="6b5f1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b5f1-108">EXAMPLES</span></span>

### <span data-ttu-id="6b5f1-109">Exemplo 1: obter detalhes para uma implantação de produção</span><span class="sxs-lookup"><span data-stu-id="6b5f1-109">Example 1: Get details for a production deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="6b5f1-110">Esse comando retorna os detalhes da implantação do serviço chamado ContosoService.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-110">This command returns the details of the deployment for the service named ContosoService.</span></span>
<span data-ttu-id="6b5f1-111">Esse comando não especifica um slot.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-111">This command does not specify a slot.</span></span>
<span data-ttu-id="6b5f1-112">Portanto, o comando usa o valor padrão de produção.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-112">Therefore, the command uses the default value of Production.</span></span>

### <span data-ttu-id="6b5f1-113">Exemplo 2: obter detalhes para uma implantação de preparo</span><span class="sxs-lookup"><span data-stu-id="6b5f1-113">Example 2: Get details for a staging deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Staging"
```

<span data-ttu-id="6b5f1-114">Esse comando retorna os detalhes da implantação de preparo do ContosoService.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-114">This command returns the details of the staging deployment of ContosoService.</span></span>

## <span data-ttu-id="6b5f1-115">OS</span><span class="sxs-lookup"><span data-stu-id="6b5f1-115">PARAMETERS</span></span>

### <span data-ttu-id="6b5f1-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="6b5f1-116">-InformationAction</span></span>
<span data-ttu-id="6b5f1-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6b5f1-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6b5f1-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b5f1-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="6b5f1-119">Continue</span></span>
- <span data-ttu-id="6b5f1-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="6b5f1-120">Ignore</span></span>
- <span data-ttu-id="6b5f1-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="6b5f1-121">Inquire</span></span>
- <span data-ttu-id="6b5f1-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6b5f1-122">SilentlyContinue</span></span>
- <span data-ttu-id="6b5f1-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="6b5f1-123">Stop</span></span>
- <span data-ttu-id="6b5f1-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="6b5f1-124">Suspend</span></span>

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

### <span data-ttu-id="6b5f1-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6b5f1-125">-InformationVariable</span></span>
<span data-ttu-id="6b5f1-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6b5f1-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6b5f1-127">-Profile</span></span>
<span data-ttu-id="6b5f1-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6b5f1-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6b5f1-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6b5f1-130">-ServiceName</span></span>
<span data-ttu-id="6b5f1-131">Especifica o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-131">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="6b5f1-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="6b5f1-132">-Slot</span></span>
<span data-ttu-id="6b5f1-133">Especifica o ambiente da implantação.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-133">Specifies the environment of the deployment.</span></span>
<span data-ttu-id="6b5f1-134">Os valores válidos são: preparação ou produção.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-134">Valid values are: Staging or Production.</span></span>
<span data-ttu-id="6b5f1-135">O valor padrão é produção.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-135">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b5f1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b5f1-136">CommonParameters</span></span>
<span data-ttu-id="6b5f1-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b5f1-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b5f1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b5f1-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b5f1-139">INPUTS</span></span>

## <span data-ttu-id="6b5f1-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b5f1-140">OUTPUTS</span></span>

## <span data-ttu-id="6b5f1-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b5f1-141">NOTES</span></span>

## <span data-ttu-id="6b5f1-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b5f1-142">RELATED LINKS</span></span>

[<span data-ttu-id="6b5f1-143">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="6b5f1-143">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="6b5f1-144">Mover-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6b5f1-144">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="6b5f1-145">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6b5f1-145">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="6b5f1-146">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6b5f1-146">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="6b5f1-147">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6b5f1-147">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


