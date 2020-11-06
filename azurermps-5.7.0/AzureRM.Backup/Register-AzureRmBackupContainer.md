---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/register-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: 71c7d883994897e4dc4b450391fb50949a125c77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432951"
---
# <span data-ttu-id="fc81a-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="fc81a-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="fc81a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc81a-102">SYNOPSIS</span></span>
<span data-ttu-id="fc81a-103">Registra o contêiner com um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="fc81a-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc81a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc81a-104">SYNTAX</span></span>

### <span data-ttu-id="fc81a-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="fc81a-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc81a-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="fc81a-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc81a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc81a-107">DESCRIPTION</span></span>
<span data-ttu-id="fc81a-108">O cmdlet **Register-AzureRmBackupContainer** registra o contêiner com um cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc81a-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="fc81a-109">Para configurar o backup usando o backup do Azure, registre primeiro o servidor ou a máquina virtual com um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="fc81a-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="fc81a-110">Esse cmdlet registra uma máquina virtual de infraestrutura como serviço (IaaS) com o cofre especificado.</span><span class="sxs-lookup"><span data-stu-id="fc81a-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="fc81a-111">A operação registrar associa a máquina virtual do Azure ao cofre de backup e controla a máquina virtual por meio do ciclo de vida do backup.</span><span class="sxs-lookup"><span data-stu-id="fc81a-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="fc81a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc81a-112">EXAMPLES</span></span>

### <span data-ttu-id="fc81a-113">Exemplo 1: registrar uma máquina virtual em um cofre de backup</span><span class="sxs-lookup"><span data-stu-id="fc81a-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="fc81a-114">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="fc81a-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="fc81a-115">O comando armazena o cofre na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="fc81a-115">The command stores the vault in the $Vault variable.</span></span>

<span data-ttu-id="fc81a-116">O segundo comando registra a máquina virtual chamada Contoso03Vm com o cofre em $Vault.</span><span class="sxs-lookup"><span data-stu-id="fc81a-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="fc81a-117">Essa máquina virtual pertence ao serviço chamado ContosoService27.</span><span class="sxs-lookup"><span data-stu-id="fc81a-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="fc81a-118">OS</span><span class="sxs-lookup"><span data-stu-id="fc81a-118">PARAMETERS</span></span>

### <span data-ttu-id="fc81a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc81a-119">-DefaultProfile</span></span>
<span data-ttu-id="fc81a-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fc81a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc81a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc81a-121">-Name</span></span>
<span data-ttu-id="fc81a-122">Especifica o nome da máquina virtual que este cmdlet registra.</span><span class="sxs-lookup"><span data-stu-id="fc81a-122">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc81a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc81a-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc81a-124">Especifica o nome do grupo de recursos para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fc81a-124">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc81a-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fc81a-125">-ServiceName</span></span>
<span data-ttu-id="fc81a-126">Especifica o nome do serviço da máquina virtual que este cmdlet registra.</span><span class="sxs-lookup"><span data-stu-id="fc81a-126">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>

<span data-ttu-id="fc81a-127">Geralmente, um nome de serviço de nuvem tem um suffix. cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="fc81a-127">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="fc81a-128">Não inclua o sufixo ao especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fc81a-128">Do not include the suffix when you specify this parameter.</span></span>

<span data-ttu-id="fc81a-129">Para obter informações sobre uma máquina virtual, use o cmdlet Get-AzureRMVM.</span><span class="sxs-lookup"><span data-stu-id="fc81a-129">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="fc81a-130">O nome do serviço é a propriedade **deploymentname** do objeto da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fc81a-130">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

```yaml
Type: String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc81a-131">-Cofre</span><span class="sxs-lookup"><span data-stu-id="fc81a-131">-Vault</span></span>
<span data-ttu-id="fc81a-132">Especifica o cofre de backup para o qual esse cmdlet registra a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fc81a-132">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="fc81a-133">Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="fc81a-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="fc81a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc81a-134">CommonParameters</span></span>
<span data-ttu-id="fc81a-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc81a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc81a-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc81a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc81a-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc81a-137">INPUTS</span></span>

### <span data-ttu-id="fc81a-138">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="fc81a-138">AzureRmBackupVault</span></span>

## <span data-ttu-id="fc81a-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc81a-139">OUTPUTS</span></span>

### <span data-ttu-id="fc81a-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="fc81a-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="fc81a-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc81a-141">NOTES</span></span>

## <span data-ttu-id="fc81a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc81a-142">RELATED LINKS</span></span>

[<span data-ttu-id="fc81a-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="fc81a-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


