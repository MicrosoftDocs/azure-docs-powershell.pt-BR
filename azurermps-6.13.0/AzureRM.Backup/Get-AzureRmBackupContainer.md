---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: e20276d8a2dfec8ffb39665e5122cfe4be74dc42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602492"
---
# <span data-ttu-id="4d91a-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4d91a-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="4d91a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d91a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d91a-103">Obtém contêineres de backup.</span><span class="sxs-lookup"><span data-stu-id="4d91a-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d91a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d91a-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d91a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d91a-105">DESCRIPTION</span></span>
<span data-ttu-id="4d91a-106">O cmdlet **Get-AzureRmBackupContainer** Obtém contêineres de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d91a-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>
<span data-ttu-id="4d91a-107">Um **AzureBackupContainer** encapsula fontes de dados, itens protegidos e pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4d91a-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="4d91a-108">Um **AzureBackupContainer** pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4d91a-108">An **AzureBackupContainer** can be one of the following:</span></span> 
- <span data-ttu-id="4d91a-109">Um computador Windows Server</span><span class="sxs-lookup"><span data-stu-id="4d91a-109">A Windows Server computer</span></span>
- <span data-ttu-id="4d91a-110">Um servidor do System Center Data Protection Manager (SCDPM)</span><span class="sxs-lookup"><span data-stu-id="4d91a-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="4d91a-111">Uma máquina virtual de infraestrutura como serviço do Azure (IaaS) antes de o backup pode fazer backup de uma fonte de dados ou item, você deve registrar o contêiner que o mantém com o serviço de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d91a-111">An Azure infrastructure as a service (IaaS) virtual machine Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="4d91a-112">O contêiner deve ser autenticado para enviar dados de backup para o cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="4d91a-112">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="4d91a-113">Para computadores com o Windows Server e servidores do SCDPM, o registro é mantido com o nome de domínio totalmente qualificado do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d91a-113">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="4d91a-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d91a-114">EXAMPLES</span></span>

### <span data-ttu-id="4d91a-115">Exemplo 1: exibir todos os servidores registrados em um cofre</span><span class="sxs-lookup"><span data-stu-id="4d91a-115">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="4d91a-116">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="4d91a-116">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="4d91a-117">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="4d91a-117">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="4d91a-118">O segundo comando obtém todos os contêineres do tipo Windows a partir do cofre no $Vault.</span><span class="sxs-lookup"><span data-stu-id="4d91a-118">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="4d91a-119">Exemplo 2: obter um contêiner específico</span><span class="sxs-lookup"><span data-stu-id="4d91a-119">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="4d91a-120">Esse comando obtém o contêiner chamado DPMSERVER. CONTOSO.COM.</span><span class="sxs-lookup"><span data-stu-id="4d91a-120">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="4d91a-121">O comando especifica o cofre no $Vault e o tipo de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4d91a-121">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="4d91a-122">Exemplo 3: exibir todas as máquinas virtuais do Azure registradas</span><span class="sxs-lookup"><span data-stu-id="4d91a-122">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="4d91a-123">Este comando obtém as máquinas virtuais registradas do cofre no $Vault.</span><span class="sxs-lookup"><span data-stu-id="4d91a-123">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="4d91a-124">OS</span><span class="sxs-lookup"><span data-stu-id="4d91a-124">PARAMETERS</span></span>

### <span data-ttu-id="4d91a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d91a-125">-DefaultProfile</span></span>
<span data-ttu-id="4d91a-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4d91a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d91a-127">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d91a-127">-ManagedResourceGroupName</span></span>
<span data-ttu-id="4d91a-128">Especifica o nome do grupo de recursos associado ao contêiner.</span><span class="sxs-lookup"><span data-stu-id="4d91a-128">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="4d91a-129">Esse nome é o mesmo valor que você especificou para o parâmetro *ServiceName* ou *ResourceGroupName* do cmdlet Register-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="4d91a-129">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d91a-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d91a-130">-Name</span></span>
<span data-ttu-id="4d91a-131">Especifica o nome do contêiner que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4d91a-131">Specifies the name of the container that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d91a-132">-Status</span><span class="sxs-lookup"><span data-stu-id="4d91a-132">-Status</span></span>
<span data-ttu-id="4d91a-133">Especifica o status atual dos contêineres que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4d91a-133">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="4d91a-134">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4d91a-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d91a-135">Não cadastrado</span><span class="sxs-lookup"><span data-stu-id="4d91a-135">NotRegistered</span></span> 
- <span data-ttu-id="4d91a-136">Removido</span><span class="sxs-lookup"><span data-stu-id="4d91a-136">Registered</span></span> 
- <span data-ttu-id="4d91a-137">Registrar</span><span class="sxs-lookup"><span data-stu-id="4d91a-137">Registering</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d91a-138">-Digite</span><span class="sxs-lookup"><span data-stu-id="4d91a-138">-Type</span></span>
<span data-ttu-id="4d91a-139">Especifica o tipo de contêiners que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4d91a-139">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d91a-140">-Cofre</span><span class="sxs-lookup"><span data-stu-id="4d91a-140">-Vault</span></span>
<span data-ttu-id="4d91a-141">Especifica um cofre de backup do qual este cmdlet obtém contêineres.</span><span class="sxs-lookup"><span data-stu-id="4d91a-141">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="4d91a-142">Para obter um **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="4d91a-142">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d91a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d91a-143">CommonParameters</span></span>
<span data-ttu-id="4d91a-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d91a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d91a-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d91a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d91a-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d91a-146">INPUTS</span></span>

### <span data-ttu-id="4d91a-147">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="4d91a-147">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="4d91a-148">Parâmetros: cofre (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d91a-148">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="4d91a-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d91a-149">OUTPUTS</span></span>

### <span data-ttu-id="4d91a-150">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4d91a-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>

## <span data-ttu-id="4d91a-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d91a-151">NOTES</span></span>
* <span data-ttu-id="4d91a-152">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4d91a-152">None</span></span>

## <span data-ttu-id="4d91a-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d91a-153">RELATED LINKS</span></span>

[<span data-ttu-id="4d91a-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4d91a-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="4d91a-155">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4d91a-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="4d91a-156">Cancelar registro-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4d91a-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


