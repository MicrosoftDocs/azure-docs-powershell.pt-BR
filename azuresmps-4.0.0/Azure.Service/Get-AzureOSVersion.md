---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945637"
---
# <span data-ttu-id="b5e85-101">Get-AzureOSVersion</span><span class="sxs-lookup"><span data-stu-id="b5e85-101">Get-AzureOSVersion</span></span>

## <span data-ttu-id="b5e85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5e85-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e85-103">Lista todos os sistemas operacionais convidados do Azure.</span><span class="sxs-lookup"><span data-stu-id="b5e85-103">Lists all Azure guest operating systems.</span></span>

## <span data-ttu-id="b5e85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5e85-104">SYNTAX</span></span>

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b5e85-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5e85-105">DESCRIPTION</span></span>
<span data-ttu-id="b5e85-106">O cmdlet **Get-AzureOSVersion** lista todos os sistemas operacionais convidados do Azure disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b5e85-106">The **Get-AzureOSVersion** cmdlet lists all the available Azure guest operating systems.</span></span>

## <span data-ttu-id="b5e85-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5e85-107">EXAMPLES</span></span>

### <span data-ttu-id="b5e85-108">Exemplo 1: obter todos os sistemas operacionais disponíveis</span><span class="sxs-lookup"><span data-stu-id="b5e85-108">Example 1: Get all available operating systems</span></span>
```
PS C:\> Get-AzureOSVersion
```

<span data-ttu-id="b5e85-109">Esse comando recupera um objeto que contém uma lista de todas as versões de sistemas operacionais convidados que estão disponíveis na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b5e85-109">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>

### <span data-ttu-id="b5e85-110">Exemplo 2: exibir as informações do sistema operacional em uma tabela</span><span class="sxs-lookup"><span data-stu-id="b5e85-110">Example 2: Display operating system information in a table</span></span>
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

<span data-ttu-id="b5e85-111">Esse comando recupera um objeto que contém uma lista de todas as versões de sistemas operacionais convidados que estão disponíveis na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b5e85-111">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>
<span data-ttu-id="b5e85-112">O comando passa a ele para o cmdlet **Format-Table** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="b5e85-112">The command passes them to the **Format-Table** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b5e85-113">Esse cmdlet formata-o como uma tabela que mostra a família do sistema operacional, o rótulo da família do sistema operacional e a versão.</span><span class="sxs-lookup"><span data-stu-id="b5e85-113">That cmdlet formats them as a table that shows the operating system family, operating system family label, and version.</span></span>

## <span data-ttu-id="b5e85-114">OS</span><span class="sxs-lookup"><span data-stu-id="b5e85-114">PARAMETERS</span></span>

### <span data-ttu-id="b5e85-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b5e85-115">-InformationAction</span></span>
<span data-ttu-id="b5e85-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b5e85-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b5e85-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b5e85-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5e85-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b5e85-118">Continue</span></span>
- <span data-ttu-id="b5e85-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b5e85-119">Ignore</span></span>
- <span data-ttu-id="b5e85-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="b5e85-120">Inquire</span></span>
- <span data-ttu-id="b5e85-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b5e85-121">SilentlyContinue</span></span>
- <span data-ttu-id="b5e85-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b5e85-122">Stop</span></span>
- <span data-ttu-id="b5e85-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b5e85-123">Suspend</span></span>

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

### <span data-ttu-id="b5e85-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b5e85-124">-InformationVariable</span></span>
<span data-ttu-id="b5e85-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b5e85-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b5e85-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b5e85-126">-Profile</span></span>
<span data-ttu-id="b5e85-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b5e85-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5e85-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b5e85-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5e85-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e85-129">CommonParameters</span></span>
<span data-ttu-id="b5e85-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5e85-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e85-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5e85-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e85-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5e85-132">INPUTS</span></span>

## <span data-ttu-id="b5e85-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5e85-133">OUTPUTS</span></span>

## <span data-ttu-id="b5e85-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5e85-134">NOTES</span></span>

## <span data-ttu-id="b5e85-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5e85-135">RELATED LINKS</span></span>

[<span data-ttu-id="b5e85-136">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="b5e85-136">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)


