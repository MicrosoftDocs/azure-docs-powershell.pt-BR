---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/get-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: 5523dd35ae91b9fea7db5f2451401793cb6059c2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946953"
---
# <span data-ttu-id="8c8b4-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="8c8b4-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="8c8b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="8c8b4-103">Obter um item de galeria específico.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-103">Get a specific gallery item.</span></span>

## <span data-ttu-id="8c8b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c8b4-104">SYNTAX</span></span>

### <span data-ttu-id="8c8b4-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="8c8b4-105">List (Default)</span></span>
```
Get-AzsGalleryItem [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8c8b4-106">Obter</span><span class="sxs-lookup"><span data-stu-id="8c8b4-106">Get</span></span>
```
Get-AzsGalleryItem -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="8c8b4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8c8b4-107">GetViaIdentity</span></span>
```
Get-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="8c8b4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c8b4-108">DESCRIPTION</span></span>
<span data-ttu-id="8c8b4-109">Obter um item de galeria específico.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-109">Get a specific gallery item.</span></span>

## <span data-ttu-id="8c8b4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c8b4-110">EXAMPLES</span></span>

### <span data-ttu-id="8c8b4-111">Exemplo 1: Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="8c8b4-111">Example 1: Get-AzsGalleryItem</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM
```

<span data-ttu-id="8c8b4-112">Obtém o item de Galeria por nome.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-112">Gets the gallery item by name.</span></span>

### <span data-ttu-id="8c8b4-113">Exemplo 2: Listar itens da Galeria</span><span class="sxs-lookup"><span data-stu-id="8c8b4-113">Example 2: List Gallery Items</span></span>
```powershell
PS C:\> Get-AzsGalleryItem

Name                                       Publisher PublisherDisplayName  ItemName                  ItemDisplayName
----                                       --------- --------------------  --------                  ---------------
Canonical.UbuntuServer1804LTS-ARM.1.0.3    Canonical Canonical             UbuntuServer1804LTS-ARM   Ubuntu Server 1...
Microsoft.AddOnRP-WindowsServer.1.1910.3   Microsoft Microsoft             AddOnRP-WindowsServer     Microsoft Azure...
Microsoft.AdminOffer.6.0.0                 Microsoft Microsoft Corporation AdminOffer                Offer
Microsoft.AvailabilitySet-ARM.1.0.1        Microsoft Microsoft             AvailabilitySet-ARM       Availability Set
Microsoft.Connection-ARM.1.2.2             Microsoft Microsoft             Connection-ARM            Connection
Microsoft.CustomScriptExtension-arm.2.0.10 Microsoft Microsoft Corp.       CustomScriptExtension-arm Custom Script E...
Microsoft.DSC-arm.2.0.7                    Microsoft Microsoft Corp.       DSC-arm                   PowerShell Desi...
Microsoft.DnsZone-ARM.1.0.1                Microsoft Microsoft             DnsZone-ARM               DNS zone
Microsoft.Image-ARM.1.0.2                  Microsoft Microsoft             Image-ARM                 Image
Microsoft.KeyVault.1.0.14                  Microsoft Microsoft             KeyVault                  Key Vault
Microsoft.LoadBalancer-ARM.1.0.2           Microsoft Microsoft             LoadBalancer-ARM          Load Balancer
Microsoft.LocalNetworkGateway-ARM.1.0.3    Microsoft Microsoft             LocalNetworkGateway-ARM   Local network g...
Microsoft.ManagedDisk-ARM.1.0.2            Microsoft Microsoft             ManagedDisk-ARM           Managed Disks
Microsoft.NetworkInterface-ARM.1.0.4       Microsoft Microsoft             NetworkInterface-ARM      Network interface
Microsoft.NetworkSecurityGroup-ARM.1.0.4   Microsoft Microsoft             NetworkSecurityGroup-ARM  Network securit...
Microsoft.Offer.6.0.0                      Microsoft Microsoft Corporation Offer                     Offer
Microsoft.Plan.6.0.0                       Microsoft Microsoft Corporation Plan                      Plan
Microsoft.PublicIPAddress-ARM.1.0.2        Microsoft Microsoft             PublicIPAddress-ARM       Public IP address
Microsoft.PublicIPPool-ARM.1.0.0           Microsoft Microsoft             PublicIPPool-ARM          Public IP pool
Microsoft.ResourceGroup.6.0.0              Microsoft Microsoft             ResourceGroup             Resource group
Microsoft.RouteTable-ARM.1.0.2             Microsoft Microsoft             RouteTable-ARM            Route table
Microsoft.ScaleUnitNode-ARM.1.0.0          Microsoft Microsoft             ScaleUnitNode-ARM         Scale Unit Node
Microsoft.Snapshot-ARM.1.0.2               Microsoft Microsoft             Snapshot-ARM              Snapshot
Microsoft.StorageAccount-ARM.101.0.1       Microsoft Microsoft             StorageAccount-ARM        Storage account
Microsoft.StorageAccount-ARM.1.0.3         Microsoft Microsoft             StorageAccount-ARM        Storage account...
Microsoft.Template.6.0.0                   Microsoft Microsoft             Template                  Template deploy...
Microsoft.TenantSubscription.6.0.0         Microsoft Microsoft Corporation TenantSubscription        Subscription
Microsoft.VirtualMachine-ARM.1.0.2         Microsoft Microsoft             VirtualMachine-ARM        Virtual machine
Microsoft.VirtualNetwork-ARM.1.0.4         Microsoft Microsoft             VirtualNetwork-ARM        Virtual network
Microsoft.VirtualNetworkGateway-ARM.1.0.3  Microsoft Microsoft             VirtualNetworkGateway-ARM Virtual network...
microsoft.antimalware-windows-arm.1.0.0    microsoft Microsoft Corp.       antimalware-windows-arm   Microsoft Antim...
microsoft.custom-script2-linux-arm.3.0.0   microsoft Microsoft Corp.       custom-script2-linux-arm  Custom Script F...
microsoft.custom-script-linux-arm.2.0.50   microsoft Microsoft Corp.       custom-script-linux-arm   Custom Script F...
microsoft.docker-arm.1.1.0                 microsoft Microsoft             docker-arm                Docker
microsoft.vmss.7.1.7                       microsoft Microsoft             vmss                      Virtual machine...

```

<span data-ttu-id="8c8b4-114">Lista todos os itens disponíveis na Galeria de pilhas do Azure.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-114">Lists all the items available in the Azure Stack gallery.</span></span>

## <span data-ttu-id="8c8b4-115">OS</span><span class="sxs-lookup"><span data-stu-id="8c8b4-115">PARAMETERS</span></span>

### <span data-ttu-id="8c8b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c8b4-116">-DefaultProfile</span></span>
<span data-ttu-id="8c8b4-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c8b4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c8b4-118">-InputObject</span></span>
<span data-ttu-id="8c8b4-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8c8b4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c8b4-120">-Name</span></span>
<span data-ttu-id="8c8b4-121">Identidade do item de galeria.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-121">Identity of the gallery item.</span></span>
<span data-ttu-id="8c8b4-122">Inclui o nome do fornecedor, o nome do item e pode incluir a versão separada por um caractere de ponto.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-122">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c8b4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c8b4-123">-PassThru</span></span>
<span data-ttu-id="8c8b4-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="8c8b4-124">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c8b4-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c8b4-125">-SubscriptionId</span></span>
<span data-ttu-id="8c8b4-126">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8c8b4-127">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c8b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c8b4-128">CommonParameters</span></span>
<span data-ttu-id="8c8b4-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c8b4-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c8b4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c8b4-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c8b4-131">INPUTS</span></span>

### <span data-ttu-id="8c8b4-132">Microsoft. Azure. PowerShell. cmdlets. Gallery. Models. IGalleryIdentity</span><span class="sxs-lookup"><span data-stu-id="8c8b4-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="8c8b4-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c8b4-133">OUTPUTS</span></span>

### <span data-ttu-id="8c8b4-134">Microsoft. Azure. PowerShell. cmdlets. Gallery. Models. Api20150401. IGalleryItem</span><span class="sxs-lookup"><span data-stu-id="8c8b4-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="8c8b4-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c8b4-135">NOTES</span></span>

<span data-ttu-id="8c8b4-136">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c8b4-137">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8c8b4-138">INPUTobject <IGalleryIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="8c8b4-138">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8c8b4-139">`[GalleryItemName <String>]`: Identidade do item de galeria.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-139">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="8c8b4-140">Inclui o nome do fornecedor, o nome do item e pode incluir a versão separada por um caractere de ponto.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-140">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="8c8b4-141">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8c8b4-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8c8b4-142">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-142">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8c8b4-143">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-143">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8c8b4-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c8b4-144">RELATED LINKS</span></span>

