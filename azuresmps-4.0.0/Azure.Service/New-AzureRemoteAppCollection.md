---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945996"
---
# <span data-ttu-id="748de-101">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="748de-101">New-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="748de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="748de-102">SYNOPSIS</span></span>
<span data-ttu-id="748de-103">Cria uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="748de-103">Creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="748de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="748de-104">SYNTAX</span></span>

### <span data-ttu-id="748de-105">AllParameterSets (padrão)</span><span class="sxs-lookup"><span data-stu-id="748de-105">AllParameterSets (Default)</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="748de-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="748de-106">AzureVNet</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="748de-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="748de-107">DESCRIPTION</span></span>
<span data-ttu-id="748de-108">O cmdlet **New-AzureRemoteAppCollection** cria uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="748de-108">The **New-AzureRemoteAppCollection** cmdlet creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="748de-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="748de-109">EXAMPLES</span></span>

### <span data-ttu-id="748de-110">Exemplo 1: criar uma coleção</span><span class="sxs-lookup"><span data-stu-id="748de-110">Example 1: Create a collection</span></span>
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

<span data-ttu-id="748de-111">Esse comando cria uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="748de-111">This command creates an Azure RemoteApp collection.</span></span>

### <span data-ttu-id="748de-112">Exemplo 2: criar uma coleção usando credenciais</span><span class="sxs-lookup"><span data-stu-id="748de-112">Example 2: Create a collection using credentials</span></span>
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

<span data-ttu-id="748de-113">Esse comando cria uma coleção do Azure RemoteApp usando uma credencial do cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="748de-113">This command creates an Azure RemoteApp collection using a credential from the **Get-Credential** cmdlet.</span></span>

## <span data-ttu-id="748de-114">OS</span><span class="sxs-lookup"><span data-stu-id="748de-114">PARAMETERS</span></span>

### <span data-ttu-id="748de-115">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="748de-115">-CollectionName</span></span>
<span data-ttu-id="748de-116">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="748de-116">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="748de-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="748de-117">-Credential</span></span>
<span data-ttu-id="748de-118">Especifica as credenciais de uma conta de serviço que tem permissão para associar os servidores RemoteApp do Azure ao seu domínio.</span><span class="sxs-lookup"><span data-stu-id="748de-118">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="748de-119">Para obter um objeto **PSCredential** , use o cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="748de-119">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="748de-120">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="748de-120">-CustomRdpProperty</span></span>
<span data-ttu-id="748de-121">Especifica as propriedades personalizadas da área de trabalho remota protocal (RDP) que podem ser usadas para configurar o redirecionamento de unidade e outras configurações.</span><span class="sxs-lookup"><span data-stu-id="748de-121">Specifies custom Remote Desktop Protocal (RDP) properties which can be used to configure drive redirection and other settings.</span></span>
<span data-ttu-id="748de-122">Consulte [configurações de RDP para serviços de área de trabalho remota no Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` para obter detalhes.  </span><span class="sxs-lookup"><span data-stu-id="748de-122">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

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

### <span data-ttu-id="748de-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="748de-123">-Description</span></span>
<span data-ttu-id="748de-124">Especifica uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="748de-124">Specifies a short description for the object.</span></span>

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

### <span data-ttu-id="748de-125">-DnsServers</span><span class="sxs-lookup"><span data-stu-id="748de-125">-DnsServers</span></span>
<span data-ttu-id="748de-126">Especifica uma lista separada por vírgulas de endereços IPv4 dos servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="748de-126">Specifies a comma-separated list of IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="748de-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="748de-127">-Domain</span></span>
<span data-ttu-id="748de-128">Especifica o nome do domínio dos serviços de domínio do Active Directory ao qual você deseja ingressar nos servidores host da sessão da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="748de-128">Specifies the name of the Active Directory Domain Services domain to which to join the RD Session Host servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="748de-129">-ImageName</span><span class="sxs-lookup"><span data-stu-id="748de-129">-ImageName</span></span>
<span data-ttu-id="748de-130">Especifica o nome da imagem de modelo do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="748de-130">Specifies the name of the Azure RemoteApp template image.</span></span>

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

### <span data-ttu-id="748de-131">-Local</span><span class="sxs-lookup"><span data-stu-id="748de-131">-Location</span></span>
<span data-ttu-id="748de-132">Especifica a região do Azure da coleção.</span><span class="sxs-lookup"><span data-stu-id="748de-132">Specifies the Azure region of the collection.</span></span>

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

### <span data-ttu-id="748de-133">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="748de-133">-OrganizationalUnit</span></span>
<span data-ttu-id="748de-134">Especifica o nome da unidade organizacional (UO) à qual você deseja ingressar nos servidores host da sessão da área de trabalho remota, por exemplo, OU = MyOu, DC = mydomain, DC = ParentDomain, DC = com.</span><span class="sxs-lookup"><span data-stu-id="748de-134">Specifies the name of the organizational unit (OU) to which to join the RD Session Host servers, for example, OU=MyOu,DC=MyDomain,DC=ParentDomain,DC=com.</span></span>
<span data-ttu-id="748de-135">Atributos como OU e DC devem estar em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="748de-135">Attributes such as OU and DC must be in uppercase.</span></span>
<span data-ttu-id="748de-136">A UO não pode ser alterada após a criação da coleção.</span><span class="sxs-lookup"><span data-stu-id="748de-136">The OU cannot be changed after the collection has been created.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="748de-137">-Plano</span><span class="sxs-lookup"><span data-stu-id="748de-137">-Plan</span></span>
<span data-ttu-id="748de-138">Especifica o plano para a coleção do Azure RemoteApp, que pode definir os limites de uso.</span><span class="sxs-lookup"><span data-stu-id="748de-138">Specifies the plan for the Azure RemoteApp collection, which may define the usage limits.</span></span>
<span data-ttu-id="748de-139">Use **Get-AzureRemoteAppPlan** para ver os planos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="748de-139">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="748de-140">-Perfil</span><span class="sxs-lookup"><span data-stu-id="748de-140">-Profile</span></span>
<span data-ttu-id="748de-141">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="748de-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="748de-142">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="748de-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="748de-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="748de-143">-ResourceType</span></span>
<span data-ttu-id="748de-144">Especifica o tipo de recurso da coleção.</span><span class="sxs-lookup"><span data-stu-id="748de-144">Specifies the resource type of the collection.</span></span>
<span data-ttu-id="748de-145">Os valores aceitáveis para esse parâmetro são: app ou desktop.</span><span class="sxs-lookup"><span data-stu-id="748de-145">The acceptable values for this parameter are: App or Desktop.</span></span>

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="748de-146">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="748de-146">-SubnetName</span></span>
<span data-ttu-id="748de-147">Especifica o nome da sub-rede na rede virtual a ser usada para criar a coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="748de-147">Specifies the name of the subnet in the virtual network to use to create the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="748de-148">-VNetName</span><span class="sxs-lookup"><span data-stu-id="748de-148">-VNetName</span></span>
<span data-ttu-id="748de-149">Especifica o nome de uma rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="748de-149">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="748de-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="748de-150">CommonParameters</span></span>
<span data-ttu-id="748de-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="748de-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="748de-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="748de-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="748de-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="748de-153">INPUTS</span></span>

## <span data-ttu-id="748de-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="748de-154">OUTPUTS</span></span>

## <span data-ttu-id="748de-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="748de-155">NOTES</span></span>

## <span data-ttu-id="748de-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="748de-156">RELATED LINKS</span></span>

[<span data-ttu-id="748de-157">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="748de-157">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="748de-158">Get-AzureRemoteAppPlan</span><span class="sxs-lookup"><span data-stu-id="748de-158">Get-AzureRemoteAppPlan</span></span>](./Get-AzureRemoteAppPlan.md)

[<span data-ttu-id="748de-159">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="748de-159">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="748de-160">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="748de-160">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="748de-161">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="748de-161">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


