---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 14B4050D-3597-4760-A152-82617B88078D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 291ea94bbdfff1da8d658074ebfb72df8943f0e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946053"
---
# <span data-ttu-id="0ed13-101">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="0ed13-101">Set-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="0ed13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ed13-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed13-103">Define as propriedades de uma coleção do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="0ed13-103">Sets the properties of a RemoteApp collection.</span></span>

## <span data-ttu-id="0ed13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ed13-104">SYNTAX</span></span>

### <span data-ttu-id="0ed13-105">DescriptionOnly (padrão)</span><span class="sxs-lookup"><span data-stu-id="0ed13-105">DescriptionOnly (Default)</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Description <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ed13-106">PlanOnly</span><span class="sxs-lookup"><span data-stu-id="0ed13-106">PlanOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Plan <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ed13-107">DomainJoined</span><span class="sxs-lookup"><span data-stu-id="0ed13-107">DomainJoined</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ed13-108">RdpPropertyOnly</span><span class="sxs-lookup"><span data-stu-id="0ed13-108">RdpPropertyOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -CustomRdpProperty <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ed13-109">AclLevelOnly</span><span class="sxs-lookup"><span data-stu-id="0ed13-109">AclLevelOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -AclLevel <CollectionAclLevel>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0ed13-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0ed13-110">DESCRIPTION</span></span>
<span data-ttu-id="0ed13-111">O cmdlet **set-AzureRemoteAppCollection** define as propriedades de uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="0ed13-111">The **Set-AzureRemoteAppCollection** cmdlet sets the properties of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="0ed13-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ed13-112">EXAMPLES</span></span>

## <span data-ttu-id="0ed13-113">OS</span><span class="sxs-lookup"><span data-stu-id="0ed13-113">PARAMETERS</span></span>

### <span data-ttu-id="0ed13-114">-AclLevel</span><span class="sxs-lookup"><span data-stu-id="0ed13-114">-AclLevel</span></span>
<span data-ttu-id="0ed13-115">Especifica o nível da lista de controle de acesso (ACL) da coleção.</span><span class="sxs-lookup"><span data-stu-id="0ed13-115">Specifies the access control list (ACL) level for the collection.</span></span>
<span data-ttu-id="0ed13-116">Os valores aceitáveis para esse parâmetro são: coleção e aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0ed13-116">The acceptable values for this parameter are: Collection and Application.</span></span>

```yaml
Type: CollectionAclLevel
Parameter Sets: AclLevelOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed13-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="0ed13-117">-CollectionName</span></span>
<span data-ttu-id="0ed13-118">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="0ed13-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed13-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="0ed13-119">-Credential</span></span>
<span data-ttu-id="0ed13-120">Especifica as credenciais de uma conta de serviço que tem permissão para associar os servidores RemoteApp do Azure ao seu domínio.</span><span class="sxs-lookup"><span data-stu-id="0ed13-120">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="0ed13-121">Para obter um objeto **PSCredential** , use o cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="0ed13-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: DomainJoined
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed13-122">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="0ed13-122">-CustomRdpProperty</span></span>
<span data-ttu-id="0ed13-123">Especifica as propriedades personalizadas de protocolo RDP que podem ser usadas para configurar o redirecionamento de unidade e outras configurações.</span><span class="sxs-lookup"><span data-stu-id="0ed13-123">Specifies custom Remote Desktop Protocol (RDP) properties which can be used to configure drive redirection and other settings.</span></span> <span data-ttu-id="0ed13-124">Consulte [configurações de RDP para serviços de área de trabalho remota no Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` para obter detalhes.  </span><span class="sxs-lookup"><span data-stu-id="0ed13-124">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: RdpPropertyOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed13-125">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0ed13-125">-Description</span></span>
<span data-ttu-id="0ed13-126">Especifica uma breve descrição para a coleção.</span><span class="sxs-lookup"><span data-stu-id="0ed13-126">Specifies a short description for the collection.</span></span>

```yaml
Type: String
Parameter Sets: DescriptionOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed13-127">-Plano</span><span class="sxs-lookup"><span data-stu-id="0ed13-127">-Plan</span></span>
<span data-ttu-id="0ed13-128">Especifica o plano para a coleção do Azure RemoteApp, que define os limites de uso.</span><span class="sxs-lookup"><span data-stu-id="0ed13-128">Specifies the plan for the Azure RemoteApp collection, which defines the usage limits.</span></span>
<span data-ttu-id="0ed13-129">Use **Get-AzureRemoteAppPlan** para ver os planos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0ed13-129">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: PlanOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed13-130">-Perfil</span><span class="sxs-lookup"><span data-stu-id="0ed13-130">-Profile</span></span>
<span data-ttu-id="0ed13-131">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="0ed13-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ed13-132">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="0ed13-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0ed13-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed13-133">CommonParameters</span></span>
<span data-ttu-id="0ed13-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ed13-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed13-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ed13-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed13-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0ed13-136">INPUTS</span></span>

## <span data-ttu-id="0ed13-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0ed13-137">OUTPUTS</span></span>

## <span data-ttu-id="0ed13-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0ed13-138">NOTES</span></span>

## <span data-ttu-id="0ed13-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ed13-139">RELATED LINKS</span></span>

[<span data-ttu-id="0ed13-140">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="0ed13-140">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="0ed13-141">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="0ed13-141">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="0ed13-142">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="0ed13-142">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


