---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8CE8F4E9-93D4-41E5-8B43-F886C018D9FB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06681544df4974a1ee906552af96302698e88d74
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945530"
---
# <span data-ttu-id="8ef3e-101">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8ef3e-101">Get-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="8ef3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ef3e-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef3e-103">Obtém as configurações do SQL Server IaaS Agent em uma máquina virtual específica.</span><span class="sxs-lookup"><span data-stu-id="8ef3e-103">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="8ef3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ef3e-104">SYNTAX</span></span>

```
Get-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8ef3e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ef3e-105">DESCRIPTION</span></span>
<span data-ttu-id="8ef3e-106">O cmdlet **Get-AzureVMSqlServerExtension** Obtém as configurações do agente do SQL Server infraestrutura como serviço (IaaS) em uma determinada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ef3e-106">The **Get-AzureVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="8ef3e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ef3e-107">EXAMPLES</span></span>

### <span data-ttu-id="8ef3e-108">Exemplo 1: obter as configurações de uma extensão do SQL Server em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8ef3e-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension-VM $VM
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="8ef3e-109">Obtém as configurações da extensão do SQL Server em uma máquina virtual específica.</span><span class="sxs-lookup"><span data-stu-id="8ef3e-109">Gets the settings of the SQL Server extension on a particular virtual machine.</span></span>

### <span data-ttu-id="8ef3e-110">Exemplo 2: obter as configurações de um agente do SQL Server IaaS em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8ef3e-110">Example 2: Get the settings of a SQL Server IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Get-AzureVMSqlServerExtension
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="8ef3e-111">Obtém as configurações do SQL Server IaaS Agent em uma determinada máquina virtual usando a entrada canalizada.</span><span class="sxs-lookup"><span data-stu-id="8ef3e-111">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine using piped input.</span></span>

### <span data-ttu-id="8ef3e-112">Exemplo 3: obter as configurações do SQL Server versão IaaS Agent específica em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8ef3e-112">Example 3: Get the settings of specific SQL Server version IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension -VM $VM -Version "1.0"
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="8ef3e-113">Esse comando obtém as configurações da versão específica do SQL Server IaaS Agent em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ef3e-113">This command gets the settings of the particular version of SQL Server IaaS Agent on a virtual machine.</span></span>

## <span data-ttu-id="8ef3e-114">OS</span><span class="sxs-lookup"><span data-stu-id="8ef3e-114">PARAMETERS</span></span>

### <span data-ttu-id="8ef3e-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8ef3e-115">-InformationAction</span></span>
<span data-ttu-id="8ef3e-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="8ef3e-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8ef3e-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8ef3e-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8ef3e-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="8ef3e-118">Continue</span></span>
- <span data-ttu-id="8ef3e-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="8ef3e-119">Ignore</span></span>
- <span data-ttu-id="8ef3e-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="8ef3e-120">Inquire</span></span>
- <span data-ttu-id="8ef3e-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8ef3e-121">SilentlyContinue</span></span>
- <span data-ttu-id="8ef3e-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="8ef3e-122">Stop</span></span>
- <span data-ttu-id="8ef3e-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="8ef3e-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ef3e-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8ef3e-124">-InformationVariable</span></span>
<span data-ttu-id="8ef3e-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="8ef3e-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ef3e-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8ef3e-126">-Profile</span></span>
<span data-ttu-id="8ef3e-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="8ef3e-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8ef3e-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="8ef3e-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8ef3e-129">-VM</span><span class="sxs-lookup"><span data-stu-id="8ef3e-129">-VM</span></span>
<span data-ttu-id="8ef3e-130">Especifica o objeto da máquina virtual persistente do qual este cmdlet obtém configurações.</span><span class="sxs-lookup"><span data-stu-id="8ef3e-130">Specifies the persistent virtual machine object that this cmdlet gets settings from.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ef3e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef3e-131">CommonParameters</span></span>
<span data-ttu-id="8ef3e-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ef3e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef3e-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ef3e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef3e-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ef3e-134">INPUTS</span></span>

## <span data-ttu-id="8ef3e-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ef3e-135">OUTPUTS</span></span>

## <span data-ttu-id="8ef3e-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ef3e-136">NOTES</span></span>

## <span data-ttu-id="8ef3e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ef3e-137">RELATED LINKS</span></span>

[<span data-ttu-id="8ef3e-138">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8ef3e-138">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="8ef3e-139">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8ef3e-139">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


