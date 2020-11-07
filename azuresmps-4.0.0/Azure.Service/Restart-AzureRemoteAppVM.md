---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F83D698B-DC48-4ACD-AD2E-4AAECBDA196B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc8081c9f81305b96b1ac227b9766352ce94b06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946084"
---
# <span data-ttu-id="e7a3c-101">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="e7a3c-101">Restart-AzureRemoteAppVM</span></span>

## <span data-ttu-id="e7a3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a3c-103">Reinicia uma máquina virtual em uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-103">Restarts a virtual machine in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="e7a3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7a3c-104">SYNTAX</span></span>

```
Restart-AzureRemoteAppVM -CollectionName <String> -UserUpn <String> [-LogoffMessage <String>]
 [-LogoffWaitSeconds <Int32>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a3c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7a3c-105">DESCRIPTION</span></span>
<span data-ttu-id="e7a3c-106">O cmdlet **Restart-AzureRemoteAppVM** reinicia uma máquina virtual em uma coleção do Azure RemoteApp na qual o usuário especificado está conectado.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-106">The **Restart-AzureRemoteAppVM** cmdlet restarts a virtual machine in an Azure RemoteApp collection on which the specified user is connected.</span></span>

## <span data-ttu-id="e7a3c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7a3c-107">EXAMPLES</span></span>

### <span data-ttu-id="e7a3c-108">Exemplo 1: reiniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e7a3c-108">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRemoteAppVM -CollectionName "ContosoVNet" -UserUPN "PattiFuller@contoso.com"
```

<span data-ttu-id="e7a3c-109">Esse comando reinicia uma máquina virtual em uma coleção do Azure RemoteApp chamada contoso.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-109">This command restarts a virtual machine in an Azure RemoteApp collection named Contoso.</span></span>
<span data-ttu-id="e7a3c-110">O usuário PattiFuller@contoso.com está conectado à coleção que contém esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-110">The user PattiFuller@contoso.com is connected to the collection which contains this virtual machine.</span></span>

## <span data-ttu-id="e7a3c-111">OS</span><span class="sxs-lookup"><span data-stu-id="e7a3c-111">PARAMETERS</span></span>

### <span data-ttu-id="e7a3c-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="e7a3c-112">-CollectionName</span></span>
<span data-ttu-id="e7a3c-113">Especifica o nome de uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-113">Specifies the name of an Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-114">-LogoffMessage</span><span class="sxs-lookup"><span data-stu-id="e7a3c-114">-LogoffMessage</span></span>
<span data-ttu-id="e7a3c-115">Especifica uma mensagem de aviso exibida para os usuários conectados à máquina virtual antes desse cmdlet desconectar-os.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-115">Specifies a warning message shown to users connected to the virtual machine before this cmdlet logs them off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-116">-LogoffWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="e7a3c-116">-LogoffWaitSeconds</span></span>
<span data-ttu-id="e7a3c-117">Especifica por quanto tempo este cmdlet aguarda antes de registrar os usuários.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-117">Specifies how long this cmdlet waits before it logs users off.</span></span>
<span data-ttu-id="e7a3c-118">O valor padrão é 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-118">The default value is 60 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e7a3c-119">-Profile</span></span>
<span data-ttu-id="e7a3c-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7a3c-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7a3c-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="e7a3c-122">-UserUpn</span></span>
<span data-ttu-id="e7a3c-123">Especifica o nome principal do usuário (UPN) do usuário para o qual esse cmdlet reinicia a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-123">Specifies the user principal name (UPN) of the user for whom this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="e7a3c-124">Para obter máquinas virtuais na coleção e nos UPNs conectados, use o cmdlet **Get-AzureRemoteAppVM** .</span><span class="sxs-lookup"><span data-stu-id="e7a3c-124">To obtain virtual machines in the collection and connected UPNs, use the **Get-AzureRemoteAppVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7a3c-125">-Confirm</span></span>
<span data-ttu-id="e7a3c-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a3c-127">-WhatIf</span></span>
<span data-ttu-id="e7a3c-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7a3c-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a3c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a3c-130">CommonParameters</span></span>
<span data-ttu-id="e7a3c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a3c-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7a3c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a3c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7a3c-133">INPUTS</span></span>

## <span data-ttu-id="e7a3c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7a3c-134">OUTPUTS</span></span>

## <span data-ttu-id="e7a3c-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7a3c-135">NOTES</span></span>

## <span data-ttu-id="e7a3c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7a3c-136">RELATED LINKS</span></span>

[<span data-ttu-id="e7a3c-137">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="e7a3c-137">Get-AzureRemoteAppVM</span></span>](./Get-AzureRemoteAppVM.md)


