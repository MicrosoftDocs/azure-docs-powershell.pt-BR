---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: abc4bce43c5be267e736cb93e03806cdd802fcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427703"
---
# <span data-ttu-id="601cc-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="601cc-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="601cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="601cc-102">SYNOPSIS</span></span>
<span data-ttu-id="601cc-103">Obtém contêineres de backup.</span><span class="sxs-lookup"><span data-stu-id="601cc-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="601cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="601cc-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="601cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="601cc-105">DESCRIPTION</span></span>
<span data-ttu-id="601cc-106">O cmdlet **Get-AzureRmBackupContainer** Obtém contêineres de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="601cc-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>

<span data-ttu-id="601cc-107">Um **AzureBackupContainer** encapsula fontes de dados, itens protegidos e pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="601cc-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="601cc-108">Um **AzureBackupContainer** pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="601cc-108">An **AzureBackupContainer** can be one of the following:</span></span> 

- <span data-ttu-id="601cc-109">Um computador Windows Server</span><span class="sxs-lookup"><span data-stu-id="601cc-109">A Windows Server computer</span></span>
- <span data-ttu-id="601cc-110">Um servidor do System Center Data Protection Manager (SCDPM)</span><span class="sxs-lookup"><span data-stu-id="601cc-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="601cc-111">Uma máquina virtual do Azure infraestrutura como serviço (IaaS)</span><span class="sxs-lookup"><span data-stu-id="601cc-111">An Azure infrastructure as a service (IaaS) virtual machine</span></span>

<span data-ttu-id="601cc-112">Antes de o backup poder fazer backup de uma fonte de dados ou item, você deve registrar o contêiner que a mantém com o serviço de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="601cc-112">Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="601cc-113">O contêiner deve ser autenticado para enviar dados de backup para o cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="601cc-113">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="601cc-114">Para computadores com o Windows Server e servidores do SCDPM, o registro é mantido com o nome de domínio totalmente qualificado do servidor.</span><span class="sxs-lookup"><span data-stu-id="601cc-114">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="601cc-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="601cc-115">EXAMPLES</span></span>

### <span data-ttu-id="601cc-116">Exemplo 1: exibir todos os servidores registrados em um cofre</span><span class="sxs-lookup"><span data-stu-id="601cc-116">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="601cc-117">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="601cc-117">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="601cc-118">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="601cc-118">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="601cc-119">O segundo comando obtém todos os contêineres do tipo Windows a partir do cofre no $Vault.</span><span class="sxs-lookup"><span data-stu-id="601cc-119">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="601cc-120">Exemplo 2: obter um contêiner específico</span><span class="sxs-lookup"><span data-stu-id="601cc-120">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="601cc-121">Esse comando obtém o contêiner chamado DPMSERVER. CONTOSO.COM.</span><span class="sxs-lookup"><span data-stu-id="601cc-121">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="601cc-122">O comando especifica o cofre no $Vault e o tipo de contêiner.</span><span class="sxs-lookup"><span data-stu-id="601cc-122">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="601cc-123">Exemplo 3: exibir todas as máquinas virtuais do Azure registradas</span><span class="sxs-lookup"><span data-stu-id="601cc-123">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="601cc-124">Este comando obtém as máquinas virtuais registradas do cofre no $Vault.</span><span class="sxs-lookup"><span data-stu-id="601cc-124">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="601cc-125">OS</span><span class="sxs-lookup"><span data-stu-id="601cc-125">PARAMETERS</span></span>

### <span data-ttu-id="601cc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="601cc-126">-DefaultProfile</span></span>
<span data-ttu-id="601cc-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="601cc-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601cc-128">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="601cc-128">-ManagedResourceGroupName</span></span>
<span data-ttu-id="601cc-129">Especifica o nome do grupo de recursos associado ao contêiner.</span><span class="sxs-lookup"><span data-stu-id="601cc-129">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="601cc-130">Esse nome é o mesmo valor que você especificou para o parâmetro *ServiceName* ou *ResourceGroupName* do cmdlet Register-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="601cc-130">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601cc-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="601cc-131">-Name</span></span>
<span data-ttu-id="601cc-132">Especifica o nome do contêiner que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="601cc-132">Specifies the name of the container that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601cc-133">-Status</span><span class="sxs-lookup"><span data-stu-id="601cc-133">-Status</span></span>
<span data-ttu-id="601cc-134">Especifica o status atual dos contêineres que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="601cc-134">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="601cc-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="601cc-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="601cc-136">Não cadastrado</span><span class="sxs-lookup"><span data-stu-id="601cc-136">NotRegistered</span></span> 
- <span data-ttu-id="601cc-137">Removido</span><span class="sxs-lookup"><span data-stu-id="601cc-137">Registered</span></span> 
- <span data-ttu-id="601cc-138">Registrar</span><span class="sxs-lookup"><span data-stu-id="601cc-138">Registering</span></span>

```yaml
Type: AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601cc-139">-Digite</span><span class="sxs-lookup"><span data-stu-id="601cc-139">-Type</span></span>
<span data-ttu-id="601cc-140">Especifica o tipo de contêiners que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="601cc-140">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601cc-141">-Cofre</span><span class="sxs-lookup"><span data-stu-id="601cc-141">-Vault</span></span>
<span data-ttu-id="601cc-142">Especifica um cofre de backup do qual este cmdlet obtém contêineres.</span><span class="sxs-lookup"><span data-stu-id="601cc-142">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="601cc-143">Para obter um **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="601cc-143">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="601cc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="601cc-144">CommonParameters</span></span>
<span data-ttu-id="601cc-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="601cc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="601cc-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="601cc-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="601cc-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="601cc-147">INPUTS</span></span>

### <span data-ttu-id="601cc-148">AzureBackupVault</span><span class="sxs-lookup"><span data-stu-id="601cc-148">AzureBackupVault</span></span>

## <span data-ttu-id="601cc-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="601cc-149">OUTPUTS</span></span>

### <span data-ttu-id="601cc-150">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="601cc-150">AzureBackupContainer</span></span>

## <span data-ttu-id="601cc-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="601cc-151">NOTES</span></span>
* <span data-ttu-id="601cc-152">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="601cc-152">None</span></span>

## <span data-ttu-id="601cc-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="601cc-153">RELATED LINKS</span></span>

[<span data-ttu-id="601cc-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="601cc-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="601cc-155">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="601cc-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="601cc-156">Cancelar registro-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="601cc-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


