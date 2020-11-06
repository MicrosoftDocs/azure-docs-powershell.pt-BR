---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: 543aa3e28d7f3dee20065a0d20f2429b3fd6d4f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428000"
---
# <span data-ttu-id="f11b3-101">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f11b3-101">Get-AzureRmBackupItem</span></span>

## <span data-ttu-id="f11b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f11b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f11b3-103">Obtém os itens em um contêiner no backup.</span><span class="sxs-lookup"><span data-stu-id="f11b3-103">Gets the items under a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f11b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f11b3-104">SYNTAX</span></span>

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f11b3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f11b3-105">DESCRIPTION</span></span>
<span data-ttu-id="f11b3-106">O cmdlet **Get-AzureRmBackupItem** Obtém os itens em um contêiner no Azure backup e o status de proteção dos itens.</span><span class="sxs-lookup"><span data-stu-id="f11b3-106">The **Get-AzureRmBackupItem** cmdlet gets the items in a container in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="f11b3-107">Habilite os itens para proteção usando o cmdlet Enable-AzureRmBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="f11b3-107">Enable items for protection by using the Enable-AzureRmBackupProtection cmdlet.</span></span>

<span data-ttu-id="f11b3-108">Um contêiner que está registrado em um cofre de backup pode ter um ou mais itens que podem ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="f11b3-108">A container that is registered to a Backup vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="f11b3-109">Para máquinas virtuais do Azure, pode haver apenas um item no contêiner da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f11b3-109">For Azure virtual machines, there can be only one item in the virtual machine container.</span></span>

## <span data-ttu-id="f11b3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f11b3-110">EXAMPLES</span></span>

### <span data-ttu-id="f11b3-111">Exemplo 1: obter os itens em um contêiner</span><span class="sxs-lookup"><span data-stu-id="f11b3-111">Example 1: Get the items in a container</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

<span data-ttu-id="f11b3-112">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="f11b3-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="f11b3-113">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="f11b3-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="f11b3-114">O segundo comando obtém um contêiner que tem o nome especificado no cofre no $Vault usando o cmdlet **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="f11b3-114">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="f11b3-115">O comando armazena esse objeto na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="f11b3-115">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="f11b3-116">O comando final Obtém o item de backup no contêiner em $Container.</span><span class="sxs-lookup"><span data-stu-id="f11b3-116">The final command gets the backup item in the container in $Container.</span></span>

### <span data-ttu-id="f11b3-117">Exemplo 2: exibir todas as propriedades de um item</span><span class="sxs-lookup"><span data-stu-id="f11b3-117">Example 2: View all properties for an item</span></span>
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

<span data-ttu-id="f11b3-118">Esse comando obtém o item de backup no contêiner em $Container e, em seguida, o passa para o cmdlet Select-Object.</span><span class="sxs-lookup"><span data-stu-id="f11b3-118">This command gets the backup item in the container in $Container, and then passes it to the Select-Object cmdlet.</span></span>
<span data-ttu-id="f11b3-119">Esse cmdlet retorna todas as propriedades do item de backup.</span><span class="sxs-lookup"><span data-stu-id="f11b3-119">That cmdlet returns all properties of the backup item.</span></span>
<span data-ttu-id="f11b3-120">Para obter mais informações, digite `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="f11b3-120">For more information, type `Get-Help Select-Object`.</span></span>

## <span data-ttu-id="f11b3-121">OS</span><span class="sxs-lookup"><span data-stu-id="f11b3-121">PARAMETERS</span></span>

### <span data-ttu-id="f11b3-122">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="f11b3-122">-Container</span></span>
<span data-ttu-id="f11b3-123">Especifica um objeto de contêiner para o qual este cmdlet obtém itens de backup.</span><span class="sxs-lookup"><span data-stu-id="f11b3-123">Specifies a container object for which this cmdlet gets backup items.</span></span>
<span data-ttu-id="f11b3-124">Para obter um **AzureRmBackupContainer** , use o cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="f11b3-124">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-125">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="f11b3-125">-ProtectionStatus</span></span>
<span data-ttu-id="f11b3-126">Especifica o status geral da proteção de um item no contêiner.</span><span class="sxs-lookup"><span data-stu-id="f11b3-126">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="f11b3-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f11b3-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f11b3-128">Protegida</span><span class="sxs-lookup"><span data-stu-id="f11b3-128">Protected</span></span> 
- <span data-ttu-id="f11b3-129">Proteção</span><span class="sxs-lookup"><span data-stu-id="f11b3-129">Protecting</span></span>  
- <span data-ttu-id="f11b3-130">Não protegido</span><span class="sxs-lookup"><span data-stu-id="f11b3-130">NotProtected</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-131">-Status</span><span class="sxs-lookup"><span data-stu-id="f11b3-131">-Status</span></span>
<span data-ttu-id="f11b3-132">Especifica o status de backup de um item.</span><span class="sxs-lookup"><span data-stu-id="f11b3-132">Specifies the backup status for an item.</span></span>
<span data-ttu-id="f11b3-133">Os valores aceitáveis para esse parâmetro são: IRPending, Protected, ProtectionError e ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="f11b3-133">The acceptable values for this parameter are: IRPending, Protected, ProtectionError, and ProtectionStopped.</span></span>
<span data-ttu-id="f11b3-134">Se o parâmetro *ProtectionStatus* tiver o valor protegido, você poderá usar o valor do parâmetro *status* para filtrar itens.</span><span class="sxs-lookup"><span data-stu-id="f11b3-134">If the *ProtectionStatus* parameter has the value Protected, you can use the *Status* parameter value to filter items.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-135">-Digite</span><span class="sxs-lookup"><span data-stu-id="f11b3-135">-Type</span></span>
<span data-ttu-id="f11b3-136">Especifica o tipo de item que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f11b3-136">Specifies the type of item that this cmdlet gets.</span></span>
<span data-ttu-id="f11b3-137">Atualmente, o único valor com suporte é AzureVM.</span><span class="sxs-lookup"><span data-stu-id="f11b3-137">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f11b3-138">-DefaultProfile</span></span>
<span data-ttu-id="f11b3-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f11b3-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f11b3-140">CommonParameters</span></span>
<span data-ttu-id="f11b3-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f11b3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f11b3-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f11b3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f11b3-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f11b3-143">INPUTS</span></span>

### <span data-ttu-id="f11b3-144">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f11b3-144">AzureRmBackupContainer</span></span>

## <span data-ttu-id="f11b3-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f11b3-145">OUTPUTS</span></span>

### <span data-ttu-id="f11b3-146">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f11b3-146">AzureRmBackupItem</span></span>

## <span data-ttu-id="f11b3-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f11b3-147">NOTES</span></span>

## <span data-ttu-id="f11b3-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f11b3-148">RELATED LINKS</span></span>

[<span data-ttu-id="f11b3-149">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f11b3-149">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="f11b3-150">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f11b3-150">Disable-AzureRmBackupProtection</span></span>](./Disable-AzureRmBackupProtection.md)

[<span data-ttu-id="f11b3-151">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f11b3-151">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="f11b3-152">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f11b3-152">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="f11b3-153">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="f11b3-153">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="f11b3-154">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f11b3-154">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)

