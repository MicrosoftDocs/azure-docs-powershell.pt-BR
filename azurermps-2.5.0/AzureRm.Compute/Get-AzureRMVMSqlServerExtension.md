---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: 6b02a83c7664fa460cd4ebd25a1754a8bc57e784
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786577"
---
# <span data-ttu-id="ad859-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ad859-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="ad859-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad859-102">SYNOPSIS</span></span>
<span data-ttu-id="ad859-103">Obtém as configurações de uma extensão do SQL Server em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ad859-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad859-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad859-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad859-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad859-105">DESCRIPTION</span></span>
<span data-ttu-id="ad859-106">O cmdlet **Get-AzureRmVMSqlServerExtension** Obtém as configurações do agente do SQL Server infraestrutura como serviço (IaaS) em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ad859-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="ad859-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad859-107">EXAMPLES</span></span>

### <span data-ttu-id="ad859-108">Exemplo 1: obter as configurações de uma extensão do SQL Server em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="ad859-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="ad859-109">Esse comando obtém as configurações da extensão do SQL Server em uma máquina virtual chamada ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="ad859-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="ad859-110">Exemplo 2: obter as configurações usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="ad859-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzureRmVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="ad859-111">Esse comando obtém a máquina virtual chamada ContosoVM22 no serviço Service08 usando o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="ad859-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="ad859-112">O comando passa os resultados para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="ad859-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="ad859-113">O comando atual Obtém as configurações do SQL Server IaaS Agent na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ad859-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="ad859-114">Exemplo 3: obter as configurações de uma versão específica do SQL Server</span><span class="sxs-lookup"><span data-stu-id="ad859-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="ad859-115">Este comando obtém as configurações da versão 1,0 da extensão do SQL Server em uma máquina virtual chamada ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="ad859-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="ad859-116">OS</span><span class="sxs-lookup"><span data-stu-id="ad859-116">PARAMETERS</span></span>

### <span data-ttu-id="ad859-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad859-117">-DefaultProfile</span></span>
<span data-ttu-id="ad859-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad859-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad859-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad859-119">-Name</span></span>
<span data-ttu-id="ad859-120">Especifica o nome do SQL Server a extensão.</span><span class="sxs-lookup"><span data-stu-id="ad859-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad859-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad859-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad859-122">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ad859-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad859-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="ad859-123">-VMName</span></span>
<span data-ttu-id="ad859-124">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ad859-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad859-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad859-125">CommonParameters</span></span>
<span data-ttu-id="ad859-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad859-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad859-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad859-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad859-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad859-128">INPUTS</span></span>

### <span data-ttu-id="ad859-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ad859-129">None</span></span>
<span data-ttu-id="ad859-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ad859-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad859-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad859-131">OUTPUTS</span></span>

### <span data-ttu-id="ad859-132">Microsoft. Azure. Commands. COMPUTE. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="ad859-132">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="ad859-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad859-133">NOTES</span></span>

## <span data-ttu-id="ad859-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad859-134">RELATED LINKS</span></span>

[<span data-ttu-id="ad859-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad859-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ad859-136">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ad859-136">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="ad859-137">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ad859-137">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


