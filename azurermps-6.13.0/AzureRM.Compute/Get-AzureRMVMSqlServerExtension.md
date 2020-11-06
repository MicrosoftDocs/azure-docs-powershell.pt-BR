---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: e17e8d55ac831fd87e9af9991b4c8ef4d9686dee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428575"
---
# <span data-ttu-id="706b8-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="706b8-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="706b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="706b8-102">SYNOPSIS</span></span>
<span data-ttu-id="706b8-103">Obtém as configurações de uma extensão do SQL Server em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="706b8-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="706b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="706b8-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="706b8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="706b8-105">DESCRIPTION</span></span>
<span data-ttu-id="706b8-106">O cmdlet **Get-AzureRmVMSqlServerExtension** Obtém as configurações do agente do SQL Server infraestrutura como serviço (IaaS) em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="706b8-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="706b8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="706b8-107">EXAMPLES</span></span>

### <span data-ttu-id="706b8-108">Exemplo 1: obter as configurações de uma extensão do SQL Server em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="706b8-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
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

<span data-ttu-id="706b8-109">Esse comando obtém as configurações da extensão do SQL Server em uma máquina virtual chamada ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="706b8-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="706b8-110">Exemplo 2: obter as configurações usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="706b8-110">Example 2: Get the settings by using the pipeline</span></span>
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

<span data-ttu-id="706b8-111">Esse comando obtém a máquina virtual chamada ContosoVM22 no serviço Service08 usando o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="706b8-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="706b8-112">O comando passa os resultados para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="706b8-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="706b8-113">O comando atual Obtém as configurações do SQL Server IaaS Agent na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="706b8-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="706b8-114">Exemplo 3: obter as configurações de uma versão específica do SQL Server</span><span class="sxs-lookup"><span data-stu-id="706b8-114">Example 3: Get the settings of specific SQL Server version</span></span>
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

<span data-ttu-id="706b8-115">Este comando obtém as configurações da versão 1,0 da extensão do SQL Server em uma máquina virtual chamada ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="706b8-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="706b8-116">OS</span><span class="sxs-lookup"><span data-stu-id="706b8-116">PARAMETERS</span></span>

### <span data-ttu-id="706b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="706b8-117">-DefaultProfile</span></span>
<span data-ttu-id="706b8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="706b8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="706b8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="706b8-119">-Name</span></span>
<span data-ttu-id="706b8-120">Especifica o nome do SQL Server a extensão.</span><span class="sxs-lookup"><span data-stu-id="706b8-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="706b8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="706b8-121">-ResourceGroupName</span></span>
<span data-ttu-id="706b8-122">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="706b8-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="706b8-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="706b8-123">-VMName</span></span>
<span data-ttu-id="706b8-124">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="706b8-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="706b8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="706b8-125">CommonParameters</span></span>
<span data-ttu-id="706b8-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="706b8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="706b8-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="706b8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="706b8-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="706b8-128">INPUTS</span></span>

### <span data-ttu-id="706b8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="706b8-129">System.String</span></span>

## <span data-ttu-id="706b8-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="706b8-130">OUTPUTS</span></span>

### <span data-ttu-id="706b8-131">Microsoft. Azure. Commands. COMPUTE. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="706b8-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="706b8-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="706b8-132">NOTES</span></span>

## <span data-ttu-id="706b8-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="706b8-133">RELATED LINKS</span></span>

[<span data-ttu-id="706b8-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="706b8-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="706b8-135">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="706b8-135">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="706b8-136">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="706b8-136">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


