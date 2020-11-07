---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1B1C1459-A602-423D-8CAA-B4901CFC2C82
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f684908e8119da007f8b1f844ebbac40713d51
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946479"
---
# <span data-ttu-id="b066b-101">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="b066b-101">Remove-AzureDns</span></span>

## <span data-ttu-id="b066b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b066b-102">SYNOPSIS</span></span>
<span data-ttu-id="b066b-103">Remove um servidor DNS de um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="b066b-103">Removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="b066b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b066b-104">SYNTAX</span></span>

```
Remove-AzureDns [-Name] <String> [-ServiceName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b066b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b066b-105">DESCRIPTION</span></span>
<span data-ttu-id="b066b-106">O cmdlet **Remove-AzureDns** remove um servidor DNS de um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="b066b-106">The **Remove-AzureDns** cmdlet removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="b066b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b066b-107">EXAMPLES</span></span>

### <span data-ttu-id="b066b-108">Exemplo 1: remover um servidor DNS de um serviço</span><span class="sxs-lookup"><span data-stu-id="b066b-108">Example 1: Remove a DNS server from a service</span></span>
```
PS C:\> Remove-AzureDns -ServiceName "ContosoService" -Name "Dns07"
```

<span data-ttu-id="b066b-109">Esse comando Remove o servidor DNS chamado Dns07 de ContosoService.</span><span class="sxs-lookup"><span data-stu-id="b066b-109">This command removes the DNS server named Dns07 from ContosoService.</span></span>

## <span data-ttu-id="b066b-110">OS</span><span class="sxs-lookup"><span data-stu-id="b066b-110">PARAMETERS</span></span>

### <span data-ttu-id="b066b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b066b-111">-Force</span></span>
<span data-ttu-id="b066b-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b066b-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b066b-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b066b-113">-InformationAction</span></span>
<span data-ttu-id="b066b-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b066b-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b066b-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b066b-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b066b-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b066b-116">Continue</span></span>
- <span data-ttu-id="b066b-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b066b-117">Ignore</span></span>
- <span data-ttu-id="b066b-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="b066b-118">Inquire</span></span>
- <span data-ttu-id="b066b-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b066b-119">SilentlyContinue</span></span>
- <span data-ttu-id="b066b-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b066b-120">Stop</span></span>
- <span data-ttu-id="b066b-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b066b-121">Suspend</span></span>

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

### <span data-ttu-id="b066b-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b066b-122">-InformationVariable</span></span>
<span data-ttu-id="b066b-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b066b-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b066b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b066b-124">-Name</span></span>
<span data-ttu-id="b066b-125">Especifica o nome do servidor DNS que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="b066b-125">Specifies the name of the DNS server that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b066b-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b066b-126">-Profile</span></span>
<span data-ttu-id="b066b-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b066b-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b066b-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b066b-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b066b-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b066b-129">-ServiceName</span></span>
<span data-ttu-id="b066b-130">Especifica o nome do serviço do qual esse cmdlet Remove um servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="b066b-130">Specifies the name of the service from which this cmdlet removes a DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b066b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b066b-131">CommonParameters</span></span>
<span data-ttu-id="b066b-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b066b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b066b-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b066b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b066b-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b066b-134">INPUTS</span></span>

## <span data-ttu-id="b066b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b066b-135">OUTPUTS</span></span>

### <span data-ttu-id="b066b-136">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="b066b-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="b066b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b066b-137">NOTES</span></span>

## <span data-ttu-id="b066b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b066b-138">RELATED LINKS</span></span>

[<span data-ttu-id="b066b-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="b066b-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="b066b-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="b066b-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="b066b-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="b066b-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="b066b-142">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="b066b-142">Set-AzureDns</span></span>](./Set-AzureDns.md)


