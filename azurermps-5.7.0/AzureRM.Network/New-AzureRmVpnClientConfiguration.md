---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 07618d546ebdadfb3313e17b881a7afbe09d1ff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432066"
---
# <span data-ttu-id="872a1-101">New-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="872a1-101">New-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="872a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="872a1-102">SYNOPSIS</span></span>
<span data-ttu-id="872a1-103">Esse comando permite que os usuários criem o pacote de perfil VPN com base em configurações de VPN pré-configuradas no gateway VPN, além de algumas configurações adicionais que os usuários podem precisar configurar, por exemplo, alguns certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="872a1-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="872a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="872a1-104">SYNTAX</span></span>

```
New-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="872a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="872a1-105">DESCRIPTION</span></span>
<span data-ttu-id="872a1-106">Isso permite que os usuários criem o pacote de perfil VPN com base em configurações de VPN pré-configuradas no gateway VPN, além de algumas configurações adicionais que os usuários podem precisar configurar, por exemplo, alguns certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="872a1-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="872a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="872a1-107">EXAMPLES</span></span>

### <span data-ttu-id="872a1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="872a1-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="872a1-109">Esse cmdlet é usado para criar um arquivo zip do perfil do cliente VPN para "ContosoVirtualNetworkGateway" no grupo de Resource "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="872a1-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="872a1-110">O perfil é gerado para um servidor RADIUS pré-configurado que é configurado para usar o método de autenticação "EAPTLS" com o arquivo de certificado VpnProfileRadiusCert.</span><span class="sxs-lookup"><span data-stu-id="872a1-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="872a1-111">OS</span><span class="sxs-lookup"><span data-stu-id="872a1-111">PARAMETERS</span></span>

### <span data-ttu-id="872a1-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="872a1-112">-AuthenticationMethod</span></span>
<span data-ttu-id="872a1-113">O método de autenticação pode ter os valores EAPMSCHAPv2 ou EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="872a1-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="872a1-114">Quando EAPMSCHAPv2 é especificado, o cmdlet gera um instalador de configuração de cliente para autenticação de nome de usuário/senha que usa o protocolo de autenticação EAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="872a1-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="872a1-115">Se EAPTLS for especificado, o cmdlet gerará um instalador de configuração de cliente para autenticação de certificado que usa o protocolo EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="872a1-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="872a1-116">A opção "EapTls" pode ser usada para autenticação de certificação e autenticação de certificado baseada em RADIUS realizada pelo gateway de rede virtual carregando a raiz confiável.</span><span class="sxs-lookup"><span data-stu-id="872a1-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="872a1-117">O cmdlet detecta automaticamente o que está configurado.</span><span class="sxs-lookup"><span data-stu-id="872a1-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872a1-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="872a1-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="872a1-119">Uma lista de caminhos de certificado raiz do cliente</span><span class="sxs-lookup"><span data-stu-id="872a1-119">A list of client root certificate paths</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872a1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872a1-120">-DefaultProfile</span></span>
<span data-ttu-id="872a1-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="872a1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="872a1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="872a1-122">-Name</span></span>
<span data-ttu-id="872a1-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="872a1-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872a1-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="872a1-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="872a1-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="872a1-125">ProcessorArchitecture</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872a1-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="872a1-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="872a1-127">Caminho do certificado raiz do servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="872a1-127">Radius server root certificate path.</span></span> <span data-ttu-id="872a1-128">Esse é um parâmetro obrigatório que deve ser especificado quando EAP-TLS com autenticação RADIUS for usado.</span><span class="sxs-lookup"><span data-stu-id="872a1-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="872a1-129">Esse é o nome do caminho completo do arquivo. cer que contém o certificado raiz RADIUS que o cliente usa para validar o servidor RADIUS durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="872a1-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="872a1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="872a1-130">-ResourceGroupName</span></span>
<span data-ttu-id="872a1-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="872a1-131">The resource group name.</span></span>

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

### <span data-ttu-id="872a1-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="872a1-132">-Confirm</span></span>
<span data-ttu-id="872a1-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="872a1-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872a1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="872a1-134">-WhatIf</span></span>
<span data-ttu-id="872a1-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="872a1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="872a1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="872a1-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872a1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872a1-137">CommonParameters</span></span>
<span data-ttu-id="872a1-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="872a1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872a1-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="872a1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872a1-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="872a1-140">INPUTS</span></span>

### <span data-ttu-id="872a1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="872a1-141">System.String</span></span>
<span data-ttu-id="872a1-142">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="872a1-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="872a1-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="872a1-143">OUTPUTS</span></span>

### <span data-ttu-id="872a1-144">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="872a1-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="872a1-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="872a1-145">NOTES</span></span>

## <span data-ttu-id="872a1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="872a1-146">RELATED LINKS</span></span>
