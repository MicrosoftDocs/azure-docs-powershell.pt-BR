---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8170AEF9-46E6-4087-8A68-29DFD5D014B5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb63d143ca2cafce92109e17fd3ced6a9dc070e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945824"
---
# <span data-ttu-id="adb50-101">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="adb50-101">Set-AzureRole</span></span>

## <span data-ttu-id="adb50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adb50-102">SYNOPSIS</span></span>
<span data-ttu-id="adb50-103">Define o número de instâncias de uma função do Azure para executar.</span><span class="sxs-lookup"><span data-stu-id="adb50-103">Sets the number of instances of an Azure role to run.</span></span>

## <span data-ttu-id="adb50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adb50-104">SYNTAX</span></span>

```
Set-AzureRole [-ServiceName] <String> [-Slot] <String> [-RoleName] <String> [-Count] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="adb50-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="adb50-105">DESCRIPTION</span></span>
<span data-ttu-id="adb50-106">O cmdlet **set-AzureRole** define o número de instâncias de uma função especificada para ser executada em uma implantação do Azure.</span><span class="sxs-lookup"><span data-stu-id="adb50-106">The **Set-AzureRole** cmdlet sets the number of instances of a specified role to run in an Azure deployment.</span></span>

## <span data-ttu-id="adb50-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adb50-107">EXAMPLES</span></span>

### <span data-ttu-id="adb50-108">1: definir o número de instâncias para uma função</span><span class="sxs-lookup"><span data-stu-id="adb50-108">1: Set the number of instances for a role</span></span>
```
PS C:\> Set-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestRole03" -Count 3
```

<span data-ttu-id="adb50-109">Esse comando define a função MyTestRole03 que está sendo executada em produção no serviço MySvc01 para ter três instâncias.</span><span class="sxs-lookup"><span data-stu-id="adb50-109">This command sets the MyTestRole03 role that is running in production on the MySvc01 service to have three instances.</span></span>

## <span data-ttu-id="adb50-110">OS</span><span class="sxs-lookup"><span data-stu-id="adb50-110">PARAMETERS</span></span>

### <span data-ttu-id="adb50-111">-Contagem</span><span class="sxs-lookup"><span data-stu-id="adb50-111">-Count</span></span>
<span data-ttu-id="adb50-112">Especifica o número de instâncias de função a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="adb50-112">Specifies the number of role instances to run.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adb50-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="adb50-113">-InformationAction</span></span>
<span data-ttu-id="adb50-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="adb50-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="adb50-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="adb50-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="adb50-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="adb50-116">Continue</span></span>
- <span data-ttu-id="adb50-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="adb50-117">Ignore</span></span>
- <span data-ttu-id="adb50-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="adb50-118">Inquire</span></span>
- <span data-ttu-id="adb50-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="adb50-119">SilentlyContinue</span></span>
- <span data-ttu-id="adb50-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="adb50-120">Stop</span></span>
- <span data-ttu-id="adb50-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="adb50-121">Suspend</span></span>

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

### <span data-ttu-id="adb50-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="adb50-122">-InformationVariable</span></span>
<span data-ttu-id="adb50-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="adb50-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="adb50-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="adb50-124">-Profile</span></span>
<span data-ttu-id="adb50-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="adb50-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="adb50-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="adb50-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="adb50-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="adb50-127">-RoleName</span></span>
<span data-ttu-id="adb50-128">Especifica o nome da função para a qual definir o número de instâncias.</span><span class="sxs-lookup"><span data-stu-id="adb50-128">Specifies the name of the role for which to set the number of instances.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adb50-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="adb50-129">-ServiceName</span></span>
<span data-ttu-id="adb50-130">Especifica o nome do serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="adb50-130">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="adb50-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="adb50-131">-Slot</span></span>
<span data-ttu-id="adb50-132">Especifica o ambiente de implantação da implantação a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="adb50-132">Specifies the deployment environment of the deployment to modify.</span></span>
<span data-ttu-id="adb50-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="adb50-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="adb50-134">Preparo</span><span class="sxs-lookup"><span data-stu-id="adb50-134">Production</span></span>
- <span data-ttu-id="adb50-135">Preparação</span><span class="sxs-lookup"><span data-stu-id="adb50-135">Staging</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adb50-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb50-136">CommonParameters</span></span>
<span data-ttu-id="adb50-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb50-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb50-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adb50-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb50-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="adb50-139">INPUTS</span></span>

## <span data-ttu-id="adb50-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="adb50-140">OUTPUTS</span></span>

## <span data-ttu-id="adb50-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="adb50-141">NOTES</span></span>

## <span data-ttu-id="adb50-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adb50-142">RELATED LINKS</span></span>

[<span data-ttu-id="adb50-143">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="adb50-143">Get-AzureRole</span></span>](./Get-AzureRole.md)


